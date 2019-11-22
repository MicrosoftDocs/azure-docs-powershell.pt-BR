---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062132"
---
## <a name="300---november-2019"></a><span data-ttu-id="11d0d-103">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="11d0d-104">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-104">General</span></span>
* <span data-ttu-id="11d0d-105">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="11d0d-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11d0d-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-106">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-107">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="11d0d-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11d0d-108">Az.Advisor</span></span>
* <span data-ttu-id="11d0d-109">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d0d-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11d0d-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11d0d-110">Az.Batch</span></span>
* <span data-ttu-id="11d0d-111">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="11d0d-112">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="11d0d-113">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="11d0d-114">O parâmetro `-ResourceFile` do **New-AzBatchTask** agora usa uma coleção de objetos do `PSResourceFile` que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="11d0d-115">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="11d0d-116">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="11d0d-117">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="11d0d-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="11d0d-118">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="11d0d-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="11d0d-119">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="11d0d-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="11d0d-120">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="11d0d-121">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="11d0d-122">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="11d0d-123">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="11d0d-124">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="11d0d-125">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="11d0d-126">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="11d0d-127">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="11d0d-128">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="11d0d-129">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="11d0d-130">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="11d0d-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="11d0d-131">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="11d0d-132">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="11d0d-133">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="11d0d-134">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="11d0d-135">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="11d0d-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="11d0d-136">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="11d0d-137">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="11d0d-138">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="11d0d-139">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="11d0d-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="11d0d-140">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="11d0d-141">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="11d0d-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="11d0d-142">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="11d0d-143">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="11d0d-144">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="11d0d-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="11d0d-145">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="11d0d-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="11d0d-146">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="11d0d-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11d0d-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-147">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-148">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="11d0d-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="11d0d-149">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="11d0d-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-150">Az.Compute</span></span>
* <span data-ttu-id="11d0d-151">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="11d0d-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="11d0d-152">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="11d0d-153">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="11d0d-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="11d0d-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="11d0d-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="11d0d-155">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11d0d-156">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="11d0d-157">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="11d0d-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="11d0d-158">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11d0d-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="11d0d-159">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="11d0d-159">Breaking changes</span></span>
    - <span data-ttu-id="11d0d-160">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="11d0d-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="11d0d-161">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="11d0d-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-162">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-163">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-165">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="11d0d-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="11d0d-166">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="11d0d-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="11d0d-167">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="11d0d-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="11d0d-168">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="11d0d-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="11d0d-169">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="11d0d-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="11d0d-170">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="11d0d-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11d0d-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11d0d-171">Az.FrontDoor</span></span>
* <span data-ttu-id="11d0d-172">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="11d0d-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11d0d-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11d0d-173">Az.HDInsight</span></span>
* <span data-ttu-id="11d0d-174">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="11d0d-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="11d0d-175">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="11d0d-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="11d0d-176">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="11d0d-177">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="11d0d-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="11d0d-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11d0d-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11d0d-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11d0d-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11d0d-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="11d0d-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="11d0d-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11d0d-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="11d0d-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11d0d-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="11d0d-183">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="11d0d-184">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="11d0d-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="11d0d-185">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="11d0d-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="11d0d-186">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="11d0d-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="11d0d-187">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="11d0d-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="11d0d-188">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="11d0d-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="11d0d-189">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="11d0d-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="11d0d-190">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="11d0d-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="11d0d-191">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="11d0d-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="11d0d-192">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="11d0d-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="11d0d-193">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="11d0d-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="11d0d-194">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="11d0d-195">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-196">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-197">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="11d0d-197">Breaking changes:</span></span>
    - <span data-ttu-id="11d0d-198">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="11d0d-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11d0d-199">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11d0d-200">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="11d0d-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11d0d-201">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11d0d-202">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="11d0d-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="11d0d-203">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="11d0d-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="11d0d-204">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="11d0d-205">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="11d0d-206">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="11d0d-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11d0d-207">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="11d0d-208">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="11d0d-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="11d0d-209">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-211">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-212">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="11d0d-213">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="11d0d-214">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-215">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-216">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-217">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-218">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-219">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="11d0d-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-220">Az.Resources</span></span>
* <span data-ttu-id="11d0d-221">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="11d0d-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-222">Az.Network</span></span>
* <span data-ttu-id="11d0d-223">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="11d0d-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="11d0d-224">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="11d0d-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="11d0d-230">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="11d0d-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="11d0d-231">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-231">New cmdlet:</span></span>
        - <span data-ttu-id="11d0d-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="11d0d-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="11d0d-233">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="11d0d-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="11d0d-234">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="11d0d-235">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="11d0d-236">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="11d0d-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="11d0d-237">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="11d0d-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="11d0d-238">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="11d0d-239">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="11d0d-240">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-240">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="11d0d-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="11d0d-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11d0d-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11d0d-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="11d0d-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="11d0d-246">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="11d0d-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="11d0d-247">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="11d0d-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11d0d-248">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="11d0d-249">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="11d0d-250">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="11d0d-251">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="11d0d-252">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="11d0d-253">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-253">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="11d0d-255">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="11d0d-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11d0d-256">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11d0d-257">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11d0d-258">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11d0d-259">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="11d0d-260">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="11d0d-261">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="11d0d-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="11d0d-262">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-262">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="11d0d-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="11d0d-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="11d0d-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="11d0d-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="11d0d-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="11d0d-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="11d0d-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="11d0d-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="11d0d-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="11d0d-269">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="11d0d-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11d0d-270">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="11d0d-271">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="11d0d-272">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="11d0d-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="11d0d-273">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="11d0d-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="11d0d-274">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="11d0d-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="11d0d-275">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="11d0d-276">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="11d0d-277">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="11d0d-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="11d0d-278">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="11d0d-279">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="11d0d-280">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-280">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="11d0d-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="11d0d-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="11d0d-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-286">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="11d0d-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-287">Az.Sql</span></span>
* <span data-ttu-id="11d0d-288">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="11d0d-289">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="11d0d-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="11d0d-290">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="11d0d-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="11d0d-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="11d0d-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="11d0d-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="11d0d-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="11d0d-293">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="11d0d-294">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="11d0d-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="11d0d-295">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="11d0d-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="11d0d-296">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-297">Az.Storage</span></span>
* <span data-ttu-id="11d0d-298">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="11d0d-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="11d0d-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="11d0d-301">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="11d0d-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="11d0d-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11d0d-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="11d0d-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11d0d-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="11d0d-304">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="11d0d-305">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-305">General</span></span>
* <span data-ttu-id="11d0d-306">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11d0d-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-307">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-308">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="11d0d-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11d0d-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-309">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-310">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="11d0d-311">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="11d0d-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-312">Az.Automation</span></span>
* <span data-ttu-id="11d0d-313">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="11d0d-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="11d0d-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11d0d-314">Az.Batch</span></span>
* <span data-ttu-id="11d0d-315">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="11d0d-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-316">Az.Compute</span></span>
* <span data-ttu-id="11d0d-317">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11d0d-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="11d0d-318">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="11d0d-319">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="11d0d-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="11d0d-320">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="11d0d-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-321">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-322">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="11d0d-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="11d0d-323">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="11d0d-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="11d0d-324">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-326">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="11d0d-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11d0d-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11d0d-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="11d0d-328">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="11d0d-329">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="11d0d-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="11d0d-330">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="11d0d-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="11d0d-331">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-332">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-333">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="11d0d-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="11d0d-334">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="11d0d-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-335">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-336">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="11d0d-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="11d0d-337">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="11d0d-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="11d0d-338">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="11d0d-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="11d0d-339">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="11d0d-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-340">Az.Network</span></span>
* <span data-ttu-id="11d0d-341">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="11d0d-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="11d0d-342">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11d0d-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="11d0d-343">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-343">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="11d0d-345">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11d0d-346">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="11d0d-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="11d0d-347">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="11d0d-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11d0d-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11d0d-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11d0d-351">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="11d0d-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="11d0d-352">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="11d0d-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="11d0d-353">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="11d0d-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="11d0d-354">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="11d0d-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11d0d-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11d0d-355">Az.RedisCache</span></span>
* <span data-ttu-id="11d0d-356">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="11d0d-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-357">Az.Sql</span></span>
* <span data-ttu-id="11d0d-358">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="11d0d-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-359">Az.Storage</span></span>
* <span data-ttu-id="11d0d-360">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="11d0d-361">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="11d0d-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11d0d-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="11d0d-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="11d0d-363">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="11d0d-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11d0d-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11d0d-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11d0d-365">Az.StorageSync</span></span>
* <span data-ttu-id="11d0d-366">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="11d0d-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-367">Az.Websites</span></span>
* <span data-ttu-id="11d0d-368">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="11d0d-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="11d0d-369">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11d0d-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-370">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-371">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="11d0d-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="11d0d-372">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="11d0d-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="11d0d-373">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-374">Az.Automation</span></span>
* <span data-ttu-id="11d0d-375">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="11d0d-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="11d0d-376">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="11d0d-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="11d0d-377">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="11d0d-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-378">Az.Compute</span></span>
* <span data-ttu-id="11d0d-379">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="11d0d-380">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11d0d-381">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="11d0d-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="11d0d-382">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="11d0d-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="11d0d-383">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="11d0d-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="11d0d-384">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="11d0d-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="11d0d-385">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="11d0d-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="11d0d-386">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="11d0d-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="11d0d-387">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="11d0d-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-388">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-389">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="11d0d-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="11d0d-390">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="11d0d-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11d0d-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11d0d-391">Az.HDInsight</span></span>
* <span data-ttu-id="11d0d-392">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="11d0d-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-393">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-394">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="11d0d-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="11d0d-395">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="11d0d-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="11d0d-396">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="11d0d-396">New cmdlets are:</span></span>
    - <span data-ttu-id="11d0d-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11d0d-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11d0d-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11d0d-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11d0d-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11d0d-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11d0d-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11d0d-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-401">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-402">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="11d0d-403">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="11d0d-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="11d0d-404">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="11d0d-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="11d0d-405">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="11d0d-406">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="11d0d-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="11d0d-407">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="11d0d-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="11d0d-408">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11d0d-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="11d0d-409">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="11d0d-410">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="11d0d-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11d0d-411">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="11d0d-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="11d0d-412">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="11d0d-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11d0d-413">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="11d0d-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="11d0d-414">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="11d0d-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="11d0d-415">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="11d0d-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="11d0d-416">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="11d0d-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="11d0d-417">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="11d0d-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="11d0d-418">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="11d0d-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="11d0d-419">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="11d0d-420">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="11d0d-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="11d0d-421">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-421">Overall improved help files</span></span>
* <span data-ttu-id="11d0d-422">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="11d0d-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-423">Az.Network</span></span>
* <span data-ttu-id="11d0d-424">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="11d0d-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="11d0d-425">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="11d0d-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="11d0d-426">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="11d0d-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="11d0d-427">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="11d0d-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="11d0d-428">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="11d0d-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="11d0d-429">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="11d0d-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="11d0d-430">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="11d0d-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="11d0d-431">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="11d0d-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="11d0d-432">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="11d0d-433">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="11d0d-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="11d0d-434">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="11d0d-435">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="11d0d-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="11d0d-436">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-436">New cmdlets</span></span>
        - <span data-ttu-id="11d0d-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="11d0d-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="11d0d-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="11d0d-439">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="11d0d-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11d0d-440">New-VpnSite</span></span>
        - <span data-ttu-id="11d0d-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11d0d-441">Update-VpnSite</span></span>
        - <span data-ttu-id="11d0d-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-442">New-VpnConnection</span></span>
        - <span data-ttu-id="11d0d-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-443">Update-VpnConnection</span></span>
* <span data-ttu-id="11d0d-444">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="11d0d-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-446">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="11d0d-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="11d0d-447">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="11d0d-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-448">Az.Resources</span></span>
* <span data-ttu-id="11d0d-449">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="11d0d-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-451">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="11d0d-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="11d0d-452">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="11d0d-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="11d0d-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11d0d-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11d0d-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11d0d-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11d0d-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11d0d-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11d0d-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11d0d-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="11d0d-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11d0d-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11d0d-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11d0d-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11d0d-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11d0d-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11d0d-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11d0d-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11d0d-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11d0d-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="11d0d-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11d0d-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11d0d-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11d0d-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11d0d-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11d0d-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11d0d-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="11d0d-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="11d0d-466">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="11d0d-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11d0d-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11d0d-467">Az.SignalR</span></span>
* <span data-ttu-id="11d0d-468">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="11d0d-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-469">Az.Sql</span></span>
* <span data-ttu-id="11d0d-470">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="11d0d-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="11d0d-471">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="11d0d-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="11d0d-472">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="11d0d-473">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="11d0d-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="11d0d-474">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="11d0d-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-475">Az.Storage</span></span>
* <span data-ttu-id="11d0d-476">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="11d0d-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="11d0d-477">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="11d0d-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="11d0d-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="11d0d-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="11d0d-480">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="11d0d-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="11d0d-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="11d0d-482">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="11d0d-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11d0d-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11d0d-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11d0d-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11d0d-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11d0d-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11d0d-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11d0d-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-487">Az.Websites</span></span>
* <span data-ttu-id="11d0d-488">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="11d0d-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="11d0d-489">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="11d0d-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="11d0d-490">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="11d0d-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="11d0d-491">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="11d0d-492">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-492">General</span></span>
* <span data-ttu-id="11d0d-493">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="11d0d-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11d0d-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-494">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-495">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="11d0d-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="11d0d-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11d0d-496">Az.Aks</span></span>
* <span data-ttu-id="11d0d-497">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="11d0d-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="11d0d-498">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="11d0d-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11d0d-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-499">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-500">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="11d0d-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="11d0d-501">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="11d0d-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="11d0d-502">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="11d0d-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="11d0d-503">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="11d0d-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="11d0d-504">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11d0d-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11d0d-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11d0d-505">Az.Batch</span></span>
* <span data-ttu-id="11d0d-506">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="11d0d-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11d0d-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-507">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-508">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="11d0d-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-509">Az.Compute</span></span>
* <span data-ttu-id="11d0d-510">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="11d0d-511">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11d0d-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="11d0d-512">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="11d0d-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="11d0d-513">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="11d0d-514">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="11d0d-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="11d0d-515">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="11d0d-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="11d0d-516">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="11d0d-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="11d0d-517">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="11d0d-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-518">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-519">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="11d0d-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="11d0d-520">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="11d0d-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="11d0d-521">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="11d0d-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="11d0d-522">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="11d0d-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-524">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11d0d-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-525">Az.EventHub</span></span>
* <span data-ttu-id="11d0d-526">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="11d0d-527">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="11d0d-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="11d0d-528">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="11d0d-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="11d0d-529">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="11d0d-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="11d0d-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11d0d-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11d0d-531">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="11d0d-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-532">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-533">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-534">Az.Network</span></span>
* <span data-ttu-id="11d0d-535">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="11d0d-536">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="11d0d-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="11d0d-537">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="11d0d-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="11d0d-538">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="11d0d-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="11d0d-539">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="11d0d-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="11d0d-540">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11d0d-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="11d0d-541">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="11d0d-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-543">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="11d0d-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="11d0d-544">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="11d0d-544">Added example</span></span>
    - <span data-ttu-id="11d0d-545">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="11d0d-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="11d0d-546">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="11d0d-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="11d0d-547">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="11d0d-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-549">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-550">Az.Resources</span></span>
* <span data-ttu-id="11d0d-551">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="11d0d-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="11d0d-552">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="11d0d-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="11d0d-553">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="11d0d-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="11d0d-554">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-555">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-556">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="11d0d-557">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="11d0d-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="11d0d-558">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="11d0d-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-560">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="11d0d-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="11d0d-561">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="11d0d-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="11d0d-562">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="11d0d-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="11d0d-563">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="11d0d-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="11d0d-564">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="11d0d-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="11d0d-565">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="11d0d-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-566">Az.Sql</span></span>
* <span data-ttu-id="11d0d-567">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="11d0d-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-568">Az.Storage</span></span>
* <span data-ttu-id="11d0d-569">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d0d-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="11d0d-570">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="11d0d-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="11d0d-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="11d0d-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11d0d-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="11d0d-573">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="11d0d-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="11d0d-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11d0d-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-575">Az.Websites</span></span>
* <span data-ttu-id="11d0d-576">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="11d0d-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="11d0d-577">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-578">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-579">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11d0d-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="11d0d-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="11d0d-581">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="11d0d-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="11d0d-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-582">Az.Automation</span></span>
* <span data-ttu-id="11d0d-583">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="11d0d-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-585">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="11d0d-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-586">Az.Compute</span></span>
* <span data-ttu-id="11d0d-587">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="11d0d-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11d0d-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11d0d-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11d0d-589">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="11d0d-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="11d0d-590">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="11d0d-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-591">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-592">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="11d0d-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="11d0d-593">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="11d0d-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11d0d-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-594">Az.EventHub</span></span>
* <span data-ttu-id="11d0d-595">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11d0d-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11d0d-596">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="11d0d-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11d0d-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-597">Az.KeyVault</span></span>
* <span data-ttu-id="11d0d-598">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="11d0d-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11d0d-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-599">Az.LogicApp</span></span>
* <span data-ttu-id="11d0d-600">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="11d0d-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="11d0d-601">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="11d0d-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="11d0d-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-602">Az.ManagedServices</span></span>
* <span data-ttu-id="11d0d-603">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="11d0d-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-604">Az.Network</span></span>
* <span data-ttu-id="11d0d-605">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="11d0d-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="11d0d-606">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-606">New cmdlets</span></span>
        - <span data-ttu-id="11d0d-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d0d-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11d0d-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11d0d-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11d0d-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="11d0d-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="11d0d-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="11d0d-615">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="11d0d-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="11d0d-616">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="11d0d-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="11d0d-617">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11d0d-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="11d0d-618">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11d0d-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="11d0d-619">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="11d0d-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="11d0d-620">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="11d0d-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="11d0d-621">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="11d0d-621">Updated cmdlets</span></span>
        - <span data-ttu-id="11d0d-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11d0d-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11d0d-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11d0d-625">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11d0d-626">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="11d0d-627">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="11d0d-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11d0d-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11d0d-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="11d0d-631">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="11d0d-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="11d0d-632">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="11d0d-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="11d0d-633">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="11d0d-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-635">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="11d0d-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="11d0d-636">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="11d0d-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-638">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11d0d-639">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="11d0d-640">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="11d0d-641">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11d0d-642">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="11d0d-643">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11d0d-644">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="11d0d-645">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11d0d-646">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="11d0d-647">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="11d0d-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-648">Az.Resources</span></span>
- <span data-ttu-id="11d0d-649">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11d0d-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="11d0d-650">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="11d0d-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-651">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-652">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11d0d-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11d0d-653">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="11d0d-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-654">Az.Sql</span></span>
* <span data-ttu-id="11d0d-655">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="11d0d-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="11d0d-656">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="11d0d-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="11d0d-657">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="11d0d-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-658">Az.Storage</span></span>
* <span data-ttu-id="11d0d-659">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="11d0d-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11d0d-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11d0d-660">Az.StorageSync</span></span>
* <span data-ttu-id="11d0d-661">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="11d0d-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="11d0d-662">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="11d0d-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-663">Az.Websites</span></span>
* <span data-ttu-id="11d0d-664">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="11d0d-665">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="11d0d-666">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="11d0d-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="11d0d-667">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-668">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-669">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="11d0d-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="11d0d-670">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="11d0d-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="11d0d-671">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="11d0d-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="11d0d-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11d0d-672">Az.Advisor</span></span>
* <span data-ttu-id="11d0d-673">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11d0d-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="11d0d-674">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="11d0d-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11d0d-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-675">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-676">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="11d0d-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="11d0d-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11d0d-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="11d0d-678">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="11d0d-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="11d0d-679">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="11d0d-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="11d0d-680">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="11d0d-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="11d0d-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11d0d-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="11d0d-682">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="11d0d-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-683">Az.Automation</span></span>
* <span data-ttu-id="11d0d-684">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="11d0d-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-685">Az.Compute</span></span>
* <span data-ttu-id="11d0d-686">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-687">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-688">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="11d0d-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11d0d-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11d0d-689">Az.EventGrid</span></span>
* <span data-ttu-id="11d0d-690">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="11d0d-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-691">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-692">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="11d0d-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-693">Az.Network</span></span>
* <span data-ttu-id="11d0d-694">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="11d0d-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="11d0d-695">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="11d0d-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11d0d-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="11d0d-697">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="11d0d-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="11d0d-698">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="11d0d-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-700">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="11d0d-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-702">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="11d0d-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-703">Az.Resources</span></span>
    - <span data-ttu-id="11d0d-704">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="11d0d-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="11d0d-705">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="11d0d-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="11d0d-706">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="11d0d-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="11d0d-707">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="11d0d-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-708">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-709">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="11d0d-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-710">Az.Sql</span></span>
* <span data-ttu-id="11d0d-711">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="11d0d-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="11d0d-712">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11d0d-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="11d0d-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11d0d-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11d0d-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11d0d-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11d0d-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11d0d-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11d0d-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="11d0d-719">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="11d0d-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-720">Az.Storage</span></span>
* <span data-ttu-id="11d0d-721">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="11d0d-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11d0d-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="11d0d-723">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="11d0d-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="11d0d-724">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="11d0d-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="11d0d-725">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="11d0d-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="11d0d-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="11d0d-728">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="11d0d-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="11d0d-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11d0d-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="11d0d-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11d0d-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11d0d-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11d0d-731">Az.StorageSync</span></span>
* <span data-ttu-id="11d0d-732">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="11d0d-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="11d0d-733">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-734">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-735">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="11d0d-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="11d0d-736">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="11d0d-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="11d0d-737">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="11d0d-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="11d0d-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11d0d-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="11d0d-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="11d0d-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-740">Az.Compute</span></span>
* <span data-ttu-id="11d0d-741">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="11d0d-742">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="11d0d-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="11d0d-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11d0d-743">Az.Dns</span></span>
* <span data-ttu-id="11d0d-744">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11d0d-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11d0d-745">Az.EventGrid</span></span>
* <span data-ttu-id="11d0d-746">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="11d0d-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="11d0d-747">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="11d0d-747">New cmdlets:</span></span>
    - <span data-ttu-id="11d0d-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11d0d-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11d0d-749">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11d0d-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11d0d-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11d0d-751">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="11d0d-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11d0d-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11d0d-753">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11d0d-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11d0d-755">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11d0d-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11d0d-757">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="11d0d-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="11d0d-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11d0d-759">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="11d0d-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="11d0d-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="11d0d-761">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="11d0d-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="11d0d-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="11d0d-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11d0d-763">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="11d0d-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="11d0d-764">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="11d0d-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="11d0d-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="11d0d-766">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11d0d-767">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11d0d-768">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="11d0d-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="11d0d-769">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11d0d-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="11d0d-770">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="11d0d-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="11d0d-771">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="11d0d-772">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="11d0d-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="11d0d-773">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="11d0d-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="11d0d-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="11d0d-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="11d0d-775">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="11d0d-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="11d0d-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="11d0d-777">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="11d0d-778">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11d0d-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11d0d-779">Az.FrontDoor</span></span>
* <span data-ttu-id="11d0d-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="11d0d-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="11d0d-781">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="11d0d-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="11d0d-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="11d0d-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="11d0d-783">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="11d0d-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-784">Az.Network</span></span>
* <span data-ttu-id="11d0d-785">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="11d0d-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="11d0d-786">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-786">New cmdlets</span></span>
        - <span data-ttu-id="11d0d-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="11d0d-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="11d0d-788">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11d0d-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="11d0d-789">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-789">New cmdlets</span></span> 
        - <span data-ttu-id="11d0d-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11d0d-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="11d0d-791">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="11d0d-792">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-792">New cmdlets</span></span> 
        - <span data-ttu-id="11d0d-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="11d0d-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11d0d-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11d0d-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11d0d-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="11d0d-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="11d0d-798">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d0d-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="11d0d-799">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-799">New cmdlets</span></span>
        - <span data-ttu-id="11d0d-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d0d-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11d0d-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d0d-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11d0d-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d0d-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11d0d-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="11d0d-804">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11d0d-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="11d0d-805">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="11d0d-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="11d0d-806">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="11d0d-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="11d0d-807">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="11d0d-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="11d0d-808">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="11d0d-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="11d0d-809">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="11d0d-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="11d0d-810">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="11d0d-811">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="11d0d-812">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="11d0d-813">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="11d0d-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="11d0d-814">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="11d0d-815">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="11d0d-816">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="11d0d-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="11d0d-817">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="11d0d-818">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="11d0d-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="11d0d-819">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="11d0d-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="11d0d-820">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11d0d-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="11d0d-821">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="11d0d-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="11d0d-822">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="11d0d-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="11d0d-823">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="11d0d-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="11d0d-824">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11d0d-825">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11d0d-826">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-828">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="11d0d-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-829">Az.Resources</span></span>
* <span data-ttu-id="11d0d-830">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="11d0d-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="11d0d-831">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11d0d-832">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11d0d-833">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="11d0d-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-835">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="11d0d-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-836">Az.Sql</span></span>
* <span data-ttu-id="11d0d-837">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11d0d-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="11d0d-838">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11d0d-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="11d0d-839">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="11d0d-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="11d0d-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11d0d-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11d0d-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11d0d-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11d0d-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11d0d-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="11d0d-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11d0d-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-845">Az.Storage</span></span>
* <span data-ttu-id="11d0d-846">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="11d0d-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="11d0d-848">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="11d0d-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="11d0d-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-850">Az.Websites</span></span>
* <span data-ttu-id="11d0d-851">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="11d0d-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="11d0d-852">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="11d0d-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="11d0d-853">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="11d0d-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-854">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-855">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="11d0d-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-856">Az.Compute</span></span>
* <span data-ttu-id="11d0d-857">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="11d0d-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="11d0d-858">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="11d0d-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11d0d-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-859">Az.EventHub</span></span>
* <span data-ttu-id="11d0d-860">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="11d0d-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="11d0d-861">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d0d-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-862">Az.Network</span></span>
* <span data-ttu-id="11d0d-863">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="11d0d-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="11d0d-864">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="11d0d-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11d0d-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="11d0d-866">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="11d0d-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-868">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="11d0d-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-869">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-870">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d0d-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-872">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="11d0d-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="11d0d-873">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-874">Az.Sql</span></span>
* <span data-ttu-id="11d0d-875">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="11d0d-876">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="11d0d-877">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11d0d-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="11d0d-878">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="11d0d-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-879">Az.Websites</span></span>
* <span data-ttu-id="11d0d-880">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="11d0d-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="11d0d-881">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11d0d-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-882">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-883">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="11d0d-884">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="11d0d-885">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="11d0d-886">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="11d0d-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="11d0d-887">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="11d0d-888">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="11d0d-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="11d0d-889">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="11d0d-890">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="11d0d-891">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="11d0d-892">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="11d0d-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="11d0d-893">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="11d0d-894">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="11d0d-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="11d0d-895">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="11d0d-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="11d0d-896">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="11d0d-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="11d0d-897">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="11d0d-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="11d0d-898">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="11d0d-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="11d0d-899">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="11d0d-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="11d0d-900">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="11d0d-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="11d0d-901">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="11d0d-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="11d0d-902">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="11d0d-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="11d0d-903">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="11d0d-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="11d0d-904">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="11d0d-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="11d0d-905">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="11d0d-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="11d0d-906">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="11d0d-907">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="11d0d-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="11d0d-908">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="11d0d-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="11d0d-909">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="11d0d-910">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="11d0d-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="11d0d-911">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="11d0d-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="11d0d-912">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="11d0d-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="11d0d-913">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="11d0d-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="11d0d-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="11d0d-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="11d0d-915">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="11d0d-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="11d0d-916">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11d0d-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11d0d-917">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="11d0d-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="11d0d-918">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="11d0d-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="11d0d-919">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="11d0d-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="11d0d-920">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="11d0d-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="11d0d-921">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="11d0d-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="11d0d-922">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11d0d-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="11d0d-923">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11d0d-924">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11d0d-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="11d0d-925">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="11d0d-926">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="11d0d-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="11d0d-927">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11d0d-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11d0d-928">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11d0d-929">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11d0d-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="11d0d-930">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="11d0d-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="11d0d-931">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="11d0d-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="11d0d-932">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="11d0d-933">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="11d0d-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="11d0d-934">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="11d0d-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="11d0d-935">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="11d0d-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="11d0d-936">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="11d0d-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="11d0d-937">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="11d0d-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="11d0d-938">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="11d0d-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="11d0d-939">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11d0d-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11d0d-940">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11d0d-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11d0d-941">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11d0d-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11d0d-942">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="11d0d-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11d0d-943">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11d0d-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11d0d-944">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11d0d-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11d0d-945">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11d0d-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11d0d-946">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="11d0d-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11d0d-947">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="11d0d-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="11d0d-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="11d0d-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="11d0d-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="11d0d-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="11d0d-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="11d0d-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="11d0d-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="11d0d-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="11d0d-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11d0d-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="11d0d-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="11d0d-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="11d0d-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11d0d-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="11d0d-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="11d0d-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="11d0d-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="11d0d-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="11d0d-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="11d0d-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11d0d-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="11d0d-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="11d0d-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-960">Az.Automation</span></span>
* <span data-ttu-id="11d0d-961">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="11d0d-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="11d0d-962">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="11d0d-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="11d0d-963">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="11d0d-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="11d0d-964">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="11d0d-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="11d0d-965">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="11d0d-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="11d0d-966">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="11d0d-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="11d0d-967">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="11d0d-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-968">Az.Compute</span></span>
* <span data-ttu-id="11d0d-969">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="11d0d-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="11d0d-970">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="11d0d-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-972">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-973">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-974">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-975">Az.Network</span></span>
* <span data-ttu-id="11d0d-976">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="11d0d-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="11d0d-977">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11d0d-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="11d0d-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="11d0d-979">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11d0d-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-980">Az.Resources</span></span>
* <span data-ttu-id="11d0d-981">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="11d0d-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-982">Az.Sql</span></span>
* <span data-ttu-id="11d0d-983">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="11d0d-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="11d0d-984">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-985">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-986">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="11d0d-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-988">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="11d0d-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="11d0d-989">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="11d0d-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-990">Az.Compute</span></span>
* <span data-ttu-id="11d0d-991">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="11d0d-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="11d0d-992">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="11d0d-993">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="11d0d-994">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="11d0d-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="11d0d-995">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="11d0d-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="11d0d-996">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11d0d-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="11d0d-997">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="11d0d-997">Breaking changes</span></span>
    - <span data-ttu-id="11d0d-998">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="11d0d-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="11d0d-999">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="11d0d-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="11d0d-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="11d0d-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="11d0d-1001">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="11d0d-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11d0d-1002">Az.Dns</span></span>
* <span data-ttu-id="11d0d-1003">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="11d0d-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="11d0d-1004">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="11d0d-1005">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11d0d-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="11d0d-1007">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="11d0d-1008">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="11d0d-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11d0d-1009">Az.HDInsight</span></span>
* <span data-ttu-id="11d0d-1010">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="11d0d-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11d0d-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="11d0d-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11d0d-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11d0d-1013">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11d0d-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11d0d-1014">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="11d0d-1015">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="11d0d-1016">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1017">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-1018">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="11d0d-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="11d0d-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="11d0d-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="11d0d-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="11d0d-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="11d0d-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="11d0d-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="11d0d-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="11d0d-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="11d0d-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="11d0d-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="11d0d-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11d0d-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11d0d-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11d0d-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11d0d-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11d0d-1030">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="11d0d-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="11d0d-1031">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="11d0d-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1032">Az.Network</span></span>
* <span data-ttu-id="11d0d-1033">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="11d0d-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="11d0d-1034">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11d0d-1034">New cmdlets</span></span>
        - <span data-ttu-id="11d0d-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="11d0d-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="11d0d-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="11d0d-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="11d0d-1039">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="11d0d-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11d0d-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="11d0d-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11d0d-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="11d0d-1042">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="11d0d-1043">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="11d0d-1044">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11d0d-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="11d0d-1046">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="11d0d-1047">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="11d0d-1048">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-1050">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="11d0d-1051">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="11d0d-1052">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="11d0d-1053">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="11d0d-1054">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="11d0d-1055">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="11d0d-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11d0d-1056">Az.Relay</span></span>
* <span data-ttu-id="11d0d-1057">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="11d0d-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-1059">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="11d0d-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1060">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1061">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="11d0d-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="11d0d-1062">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="11d0d-1063">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="11d0d-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="11d0d-1065">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="11d0d-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="11d0d-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="11d0d-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1069">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1070">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="11d0d-1071">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="11d0d-1072">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11d0d-1073">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11d0d-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="11d0d-1074">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="11d0d-1075">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11d0d-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11d0d-1076">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11d0d-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11d0d-1077">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11d0d-1078">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11d0d-1079">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11d0d-1080">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11d0d-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1081">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1082">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="11d0d-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11d0d-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11d0d-1083">Az.Batch</span></span>
* <span data-ttu-id="11d0d-1084">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11d0d-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-1085">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-1086">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-1088">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1089">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1090">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="11d0d-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="11d0d-1091">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1092">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11d0d-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-1093">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-1094">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1096">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11d0d-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11d0d-1097">Az.EventGrid</span></span>
* <span data-ttu-id="11d0d-1098">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11d0d-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1099">Az.EventHub</span></span>
* <span data-ttu-id="11d0d-1100">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="11d0d-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="11d0d-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11d0d-1101">Az.HDInsight</span></span>
* <span data-ttu-id="11d0d-1102">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1103">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-1104">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11d0d-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1105">Az.KeyVault</span></span>
* <span data-ttu-id="11d0d-1106">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1107">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11d0d-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="11d0d-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11d0d-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="11d0d-1109">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="11d0d-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11d0d-1110">Az.Media</span></span>
* <span data-ttu-id="11d0d-1111">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1112">Az.Monitor</span></span>
  * <span data-ttu-id="11d0d-1113">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="11d0d-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="11d0d-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="11d0d-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="11d0d-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="11d0d-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="11d0d-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11d0d-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11d0d-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="11d0d-1119">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="11d0d-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1120">Az.Network</span></span>
* <span data-ttu-id="11d0d-1121">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1122">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11d0d-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="11d0d-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="11d0d-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="11d0d-1124">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-1126">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="11d0d-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="11d0d-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="11d0d-1128">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-1130">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1131">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="11d0d-1132">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="11d0d-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="11d0d-1133">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="11d0d-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11d0d-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11d0d-1134">Az.RedisCache</span></span>
* <span data-ttu-id="11d0d-1135">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1136">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1137">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11d0d-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1138">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1139">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="11d0d-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="11d0d-1140">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1141">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="11d0d-1142">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="11d0d-1143">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="11d0d-1144">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="11d0d-1145">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11d0d-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1146">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1147">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="11d0d-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="11d0d-1148">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11d0d-1149">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="11d0d-1150">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="11d0d-1151">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11d0d-1152">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11d0d-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="11d0d-1153">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="11d0d-1154">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11d0d-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11d0d-1155">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11d0d-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11d0d-1156">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11d0d-1157">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11d0d-1158">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11d0d-1159">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11d0d-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1160">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1161">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="11d0d-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11d0d-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="11d0d-1163">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="11d0d-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="11d0d-1164">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="11d0d-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1165">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1166">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="11d0d-1167">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="11d0d-1168">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1169">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1170">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11d0d-1171">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="11d0d-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="11d0d-1173">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="11d0d-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-1174">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-1175">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="11d0d-1176">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1177">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1178">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="11d0d-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="11d0d-1179">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="11d0d-1180">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="11d0d-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="11d0d-1181">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11d0d-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="11d0d-1182">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="11d0d-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="11d0d-1183">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11d0d-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1184">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1185">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1186">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1187">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="11d0d-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11d0d-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="11d0d-1189">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="11d0d-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11d0d-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11d0d-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11d0d-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11d0d-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="11d0d-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="11d0d-1194">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="11d0d-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11d0d-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11d0d-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="11d0d-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11d0d-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="11d0d-1199">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11d0d-1200">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11d0d-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="11d0d-1201">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="11d0d-1202">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11d0d-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11d0d-1203">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11d0d-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11d0d-1204">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11d0d-1205">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11d0d-1206">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11d0d-1207">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11d0d-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1208">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1209">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="11d0d-1210">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="11d0d-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="11d0d-1211">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="11d0d-1211">Pre-Post script</span></span>
    * <span data-ttu-id="11d0d-1212">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="11d0d-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1213">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1214">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="11d0d-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="11d0d-1215">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11d0d-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1216">Az.KeyVault</span></span>
* <span data-ttu-id="11d0d-1217">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1218">Az.Network</span></span>
* <span data-ttu-id="11d0d-1219">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="11d0d-1220">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="11d0d-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-1222">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="11d0d-1223">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="11d0d-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1224">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1225">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11d0d-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="11d0d-1226">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="11d0d-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1227">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1228">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1229">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1230">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="11d0d-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11d0d-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11d0d-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11d0d-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="11d0d-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="11d0d-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="11d0d-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="11d0d-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1237">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1238">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="11d0d-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="11d0d-1239">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1240">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1241">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="11d0d-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="11d0d-1242">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1243">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1244">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="11d0d-1245">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="11d0d-1246">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="11d0d-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11d0d-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-1247">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-1248">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1249">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1250">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="11d0d-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-1251">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-1252">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11d0d-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-1253">Az.LogicApp</span></span>
* <span data-ttu-id="11d0d-1254">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1255">Az.Network</span></span>
* <span data-ttu-id="11d0d-1256">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-1258">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="11d0d-1259">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="11d0d-1259">SDK Update</span></span>
* <span data-ttu-id="11d0d-1260">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11d0d-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="11d0d-1261">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11d0d-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1262">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1263">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="11d0d-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="11d0d-1264">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="11d0d-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="11d0d-1265">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="11d0d-1266">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="11d0d-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="11d0d-1267">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="11d0d-1268">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="11d0d-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1269">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1270">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="11d0d-1271">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1272">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1273">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="11d0d-1274">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="11d0d-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="11d0d-1276">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1277">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1278">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="11d0d-1279">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="11d0d-1280">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-1282">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1283">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1284">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="11d0d-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="11d0d-1285">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="11d0d-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="11d0d-1286">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="11d0d-1287">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1289">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11d0d-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1290">Az.EventHub</span></span>
* <span data-ttu-id="11d0d-1291">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="11d0d-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1292">Az.KeyVault</span></span>
* <span data-ttu-id="11d0d-1293">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11d0d-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11d0d-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-1294">Az.LogicApp</span></span>
* <span data-ttu-id="11d0d-1295">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="11d0d-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="11d0d-1296">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="11d0d-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="11d0d-1297">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="11d0d-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="11d0d-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11d0d-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11d0d-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11d0d-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11d0d-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11d0d-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11d0d-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11d0d-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="11d0d-1302">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="11d0d-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="11d0d-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11d0d-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11d0d-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11d0d-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="11d0d-1307">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11d0d-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1308">Az.Monitor</span></span>
* <span data-ttu-id="11d0d-1309">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="11d0d-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1310">Az.Network</span></span>
* <span data-ttu-id="11d0d-1311">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="11d0d-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="11d0d-1313">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="11d0d-1314">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="11d0d-1315">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="11d0d-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1316">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1317">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="11d0d-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11d0d-1318">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="11d0d-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="11d0d-1319">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="11d0d-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="11d0d-1320">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="11d0d-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1321">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1322">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="11d0d-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="11d0d-1323">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="11d0d-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1324">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1325">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="11d0d-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="11d0d-1326">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1327">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1328">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11d0d-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11d0d-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="11d0d-1330">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1331">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1332">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="11d0d-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="11d0d-1333">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="11d0d-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="11d0d-1334">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="11d0d-1336">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1337">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1338">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="11d0d-1339">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="11d0d-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11d0d-1340">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="11d0d-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="11d0d-1341">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="11d0d-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1342">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1343">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="11d0d-1344">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="11d0d-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="11d0d-1345">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="11d0d-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="11d0d-1346">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1347">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1348">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="11d0d-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11d0d-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="11d0d-1350">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="11d0d-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="11d0d-1352">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="11d0d-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="11d0d-1353">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1354">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1355">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11d0d-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11d0d-1356">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11d0d-1357">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="11d0d-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="11d0d-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11d0d-1358">Az.Aks</span></span>
* <span data-ttu-id="11d0d-1359">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11d0d-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1360">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1361">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="11d0d-1362">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11d0d-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11d0d-1363">Az.Cdn</span></span>
* <span data-ttu-id="11d0d-1364">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1365">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1366">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="11d0d-1367">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11d0d-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="11d0d-1368">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="11d0d-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11d0d-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11d0d-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11d0d-1370">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11d0d-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11d0d-1371">Az.DataFactory</span></span>
* <span data-ttu-id="11d0d-1372">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="11d0d-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1374">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="11d0d-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="11d0d-1375">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="11d0d-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="11d0d-1376">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1377">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-1378">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11d0d-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1379">Az.KeyVault</span></span>
* <span data-ttu-id="11d0d-1380">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1381">Az.Network</span></span>
* <span data-ttu-id="11d0d-1382">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1383">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1384">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="11d0d-1385">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="11d0d-1386">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="11d0d-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="11d0d-1387">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="11d0d-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="11d0d-1388">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="11d0d-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="11d0d-1389">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="11d0d-1390">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="11d0d-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-1392">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="11d0d-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="11d0d-1393">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1393">Fix some error messages.</span></span>
* <span data-ttu-id="11d0d-1394">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="11d0d-1395">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11d0d-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11d0d-1396">Az.SignalR</span></span>
* <span data-ttu-id="11d0d-1397">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1398">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1399">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11d0d-1400">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="11d0d-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="11d0d-1401">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="11d0d-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="11d0d-1402">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="11d0d-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1403">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1404">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11d0d-1405">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="11d0d-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="11d0d-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="11d0d-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="11d0d-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="11d0d-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="11d0d-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="11d0d-1409">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1410">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1411">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11d0d-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11d0d-1412">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="11d0d-1413">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="11d0d-1414">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11d0d-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11d0d-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1415">Az.Accounts</span></span>
* <span data-ttu-id="11d0d-1416">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="11d0d-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1417">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1418">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="11d0d-1419">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11d0d-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="11d0d-1420">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1422">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="11d0d-1423">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="11d0d-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11d0d-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11d0d-1424">Az.EventGrid</span></span>
* <span data-ttu-id="11d0d-1425">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="11d0d-1426">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="11d0d-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="11d0d-1427">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11d0d-1428">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="11d0d-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11d0d-1429">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11d0d-1430">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="11d0d-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="11d0d-1431">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11d0d-1432">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="11d0d-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11d0d-1433">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11d0d-1434">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="11d0d-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="11d0d-1435">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="11d0d-1436">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11d0d-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1437">Az.IotHub</span></span>
* <span data-ttu-id="11d0d-1438">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="11d0d-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11d0d-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11d0d-1439">Az.LogicApp</span></span>
* <span data-ttu-id="11d0d-1440">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="11d0d-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1441">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1442">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="11d0d-1443">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="11d0d-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="11d0d-1444">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11d0d-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11d0d-1445">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="11d0d-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="11d0d-1446">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="11d0d-1447">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="11d0d-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11d0d-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11d0d-1448">Az.SignalR</span></span>
* <span data-ttu-id="11d0d-1449">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1450">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1451">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11d0d-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1452">Az.Storage</span></span>
* <span data-ttu-id="11d0d-1453">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="11d0d-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="11d0d-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11d0d-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="11d0d-1455">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="11d0d-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="11d0d-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1457">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1458">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="11d0d-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="11d0d-1459">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="11d0d-1460">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="11d0d-1461">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-1461">General</span></span>

- <span data-ttu-id="11d0d-1462">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="11d0d-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="11d0d-1463">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1463">Online help for each module</span></span>
- <span data-ttu-id="11d0d-1464">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="11d0d-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="11d0d-1465">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="11d0d-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="11d0d-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1466">Az.Accounts</span></span>
- <span data-ttu-id="11d0d-1467">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="11d0d-1468">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="11d0d-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11d0d-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="11d0d-1470">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="11d0d-1470">Fixes for #7002</span></span>
- <span data-ttu-id="11d0d-1471">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="11d0d-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11d0d-1472">Az.Batch</span></span>
- <span data-ttu-id="11d0d-1473">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="11d0d-1474">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="11d0d-1475">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="11d0d-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11d0d-1476">Az.Billing</span></span>
- <span data-ttu-id="11d0d-1477">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="11d0d-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="11d0d-1479">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="11d0d-1480">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="11d0d-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11d0d-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="11d0d-1482">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="11d0d-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="11d0d-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="11d0d-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="11d0d-1484">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="11d0d-1486">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="11d0d-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1487">Az.Monitor</span></span>
- <span data-ttu-id="11d0d-1488">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="11d0d-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11d0d-1489">Az.KeyVault</span></span>
- <span data-ttu-id="11d0d-1490">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="11d0d-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="11d0d-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11d0d-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="11d0d-1492">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="11d0d-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11d0d-1493">Az.Media</span></span>
- <span data-ttu-id="11d0d-1494">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11d0d-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11d0d-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1495">Az.Network</span></span>
<span data-ttu-id="11d0d-1496">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="11d0d-1497">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11d0d-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="11d0d-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="11d0d-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="11d0d-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="11d0d-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="11d0d-1506">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="11d0d-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11d0d-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="11d0d-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11d0d-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11d0d-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11d0d-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="11d0d-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="11d0d-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="11d0d-1513">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11d0d-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="11d0d-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11d0d-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11d0d-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11d0d-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11d0d-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11d0d-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="11d0d-1517">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="11d0d-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="11d0d-1518">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="11d0d-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="11d0d-1520">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="11d0d-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1521">Az.Profile</span></span>
- <span data-ttu-id="11d0d-1522">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11d0d-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="11d0d-1524">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="11d0d-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1525">Az.Resources</span></span>
- <span data-ttu-id="11d0d-1526">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11d0d-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="11d0d-1528">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="11d0d-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="11d0d-1529">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="11d0d-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="11d0d-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="11d0d-1531">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="11d0d-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="11d0d-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1532">Az.Sql</span></span>
- <span data-ttu-id="11d0d-1533">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="11d0d-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="11d0d-1534">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="11d0d-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="11d0d-1535">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="11d0d-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1536">Az.Storage</span></span>
- <span data-ttu-id="11d0d-1537">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11d0d-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1538">Az.Websites</span></span>
- <span data-ttu-id="11d0d-1539">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11d0d-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="11d0d-1540">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="11d0d-1541">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-1541">General</span></span>

* <span data-ttu-id="11d0d-1542">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="11d0d-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="11d0d-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1543">Az.Compute</span></span>

* <span data-ttu-id="11d0d-1544">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="11d0d-1546">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="11d0d-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="11d0d-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11d0d-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="11d0d-1548">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="11d0d-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="11d0d-1549">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="11d0d-1550">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11d0d-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="11d0d-1552">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="11d0d-1553">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="11d0d-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1554">Az.Resources</span></span>

* <span data-ttu-id="11d0d-1555">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="11d0d-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="11d0d-1556">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="11d0d-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1557">Az.Sql</span></span>

* <span data-ttu-id="11d0d-1558">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="11d0d-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="11d0d-1559">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="11d0d-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="11d0d-1560">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="11d0d-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1561">Az.Storage</span></span>

* <span data-ttu-id="11d0d-1562">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="11d0d-1563">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="11d0d-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="11d0d-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11d0d-1565">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="11d0d-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="11d0d-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11d0d-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="11d0d-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11d0d-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11d0d-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1568">Az.Websites</span></span>

* <span data-ttu-id="11d0d-1569">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="11d0d-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="11d0d-1570">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="11d0d-1571">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="11d0d-1572">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11d0d-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d0d-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="11d0d-1574">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="11d0d-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11d0d-1575">Az.Automation</span></span>
* <span data-ttu-id="11d0d-1576">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="11d0d-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="11d0d-1577">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="11d0d-1578">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="11d0d-1579">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="11d0d-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="11d0d-1580">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="11d0d-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="11d0d-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1581">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1582">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="11d0d-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="11d0d-1583">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11d0d-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="11d0d-1585">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="11d0d-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11d0d-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11d0d-1587">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="11d0d-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11d0d-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1588">Az.Network</span></span>
* <span data-ttu-id="11d0d-1589">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="11d0d-1590">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="11d0d-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="11d0d-1591">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="11d0d-1592">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="11d0d-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="11d0d-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="11d0d-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="11d0d-1594">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="11d0d-1595">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="11d0d-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="11d0d-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="11d0d-1597">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11d0d-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="11d0d-1598">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11d0d-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="11d0d-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11d0d-1599">Az.Relay</span></span>
* <span data-ttu-id="11d0d-1600">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="11d0d-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1601">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1602">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="11d0d-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="11d0d-1603">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="11d0d-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="11d0d-1604">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="11d0d-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11d0d-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-1606">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="11d0d-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="11d0d-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1607">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1608">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="11d0d-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="11d0d-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11d0d-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11d0d-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11d0d-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11d0d-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11d0d-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11d0d-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11d0d-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11d0d-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11d0d-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11d0d-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11d0d-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11d0d-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="11d0d-1617">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="11d0d-1618">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="11d0d-1619">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="11d0d-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11d0d-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11d0d-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="11d0d-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="11d0d-1624">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11d0d-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="11d0d-1625">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="11d0d-1626">Geral</span><span class="sxs-lookup"><span data-stu-id="11d0d-1626">General</span></span>
* <span data-ttu-id="11d0d-1627">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="11d0d-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="11d0d-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1628">Az.Profile</span></span>
* <span data-ttu-id="11d0d-1629">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11d0d-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="11d0d-1630">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="11d0d-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="11d0d-1631">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="11d0d-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="11d0d-1632">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="11d0d-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="11d0d-1633">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="11d0d-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="11d0d-1634">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="11d0d-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="11d0d-1635">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="11d0d-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-1637">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1638">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1639">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="11d0d-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="11d0d-1640">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="11d0d-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="11d0d-1641">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1643">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="11d0d-1644">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="11d0d-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1645">Az.Insights</span></span>
* <span data-ttu-id="11d0d-1646">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="11d0d-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="11d0d-1647">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="11d0d-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="11d0d-1648">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="11d0d-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="11d0d-1649">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="11d0d-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1650">Az.Network</span></span>
* <span data-ttu-id="11d0d-1651">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="11d0d-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="11d0d-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="11d0d-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="11d0d-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11d0d-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="11d0d-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="11d0d-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="11d0d-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="11d0d-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11d0d-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11d0d-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11d0d-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="11d0d-1659">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="11d0d-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1660">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1661">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="11d0d-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="11d0d-1662">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="11d0d-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11d0d-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11d0d-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="11d0d-1664">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11d0d-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11d0d-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="11d0d-1666">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="11d0d-1667">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="11d0d-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="11d0d-1668">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="11d0d-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="11d0d-1669">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="11d0d-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="11d0d-1670">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="11d0d-1671">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="11d0d-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1672">Az.Profile</span></span>
* <span data-ttu-id="11d0d-1673">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="11d0d-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="11d0d-1674">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11d0d-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1675">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1676">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="11d0d-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="11d0d-1677">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11d0d-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11d0d-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="11d0d-1679">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11d0d-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="11d0d-1680">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="11d0d-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11d0d-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11d0d-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1684">Az.Network</span></span>
* <span data-ttu-id="11d0d-1685">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="11d0d-1686">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1687">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1688">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="11d0d-1689">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="11d0d-1690">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="11d0d-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1691">Azure.Storage</span></span>
* <span data-ttu-id="11d0d-1692">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="11d0d-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="11d0d-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11d0d-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11d0d-1695">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="11d0d-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="11d0d-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="11d0d-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11d0d-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="11d0d-1698">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11d0d-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11d0d-1699">Az.Compute</span></span>
* <span data-ttu-id="11d0d-1700">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="11d0d-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="11d0d-1701">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="11d0d-1702">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="11d0d-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="11d0d-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="11d0d-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="11d0d-1704">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11d0d-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11d0d-1705">Az.Network</span></span>
* <span data-ttu-id="11d0d-1706">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="11d0d-1707">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="11d0d-1707">new cmdlets added</span></span>
    - <span data-ttu-id="11d0d-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="11d0d-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="11d0d-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="11d0d-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11d0d-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="11d0d-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="11d0d-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="11d0d-1714">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="11d0d-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="11d0d-1715">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="11d0d-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="11d0d-1716">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="11d0d-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11d0d-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11d0d-1717">Az.RedisCache</span></span>
* <span data-ttu-id="11d0d-1718">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="11d0d-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="11d0d-1719">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="11d0d-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="11d0d-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11d0d-1720">Az.Resources</span></span>
* <span data-ttu-id="11d0d-1721">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11d0d-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11d0d-1722">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="11d0d-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="11d0d-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11d0d-1723">Az.Sql</span></span>
* <span data-ttu-id="11d0d-1724">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="11d0d-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11d0d-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11d0d-1725">Az.Websites</span></span>
* <span data-ttu-id="11d0d-1726">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="11d0d-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="11d0d-1727">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="11d0d-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="11d0d-1728">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11d0d-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="11d0d-1729">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="11d0d-1729">Initial Release</span></span>
