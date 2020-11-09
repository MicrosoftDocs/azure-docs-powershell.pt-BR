---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283992"
---
# <span data-ttu-id="10ca2-101">Módulo AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="10ca2-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="10ca2-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="10ca2-102">Description</span></span>
<span data-ttu-id="10ca2-103">Os cmdlets no módulo de sincronização de armazenamento permitem que você gerencie as operações pertinentes à sincronização do Azure File no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10ca2-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="10ca2-104">Cmdlets AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="10ca2-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="10ca2-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="10ca2-106">Esse comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="10ca2-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="10ca2-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="10ca2-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="10ca2-108">Esse comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ca2-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="10ca2-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="10ca2-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="10ca2-110">Esse comando lista todos os servidores registrados para um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ca2-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="10ca2-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="10ca2-112">Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="10ca2-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="10ca2-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="10ca2-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="10ca2-114">Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.</span><span class="sxs-lookup"><span data-stu-id="10ca2-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="10ca2-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="10ca2-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="10ca2-116">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="10ca2-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="10ca2-117">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="10ca2-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="10ca2-118">No máximo 10.000 alterações podem ser detectadas.</span><span class="sxs-lookup"><span data-stu-id="10ca2-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="10ca2-119">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro de um limite de alterações do 10.000.</span><span class="sxs-lookup"><span data-stu-id="10ca2-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="10ca2-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="10ca2-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="10ca2-121">Verifica possíveis problemas de compatibilidade entre o sistema e a sincronização de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="10ca2-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="10ca2-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="10ca2-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="10ca2-123">Esse comando recupera novamente todos os arquivos em camadas para o disco local.</span><span class="sxs-lookup"><span data-stu-id="10ca2-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="10ca2-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="10ca2-125">Esse comando cria um ponto de extremidade da nuvem do Azure File Sync em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="10ca2-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="10ca2-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="10ca2-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="10ca2-127">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="10ca2-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="10ca2-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="10ca2-129">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="10ca2-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="10ca2-130">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="10ca2-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="10ca2-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="10ca2-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="10ca2-132">Esse comando cria um novo serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10ca2-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="10ca2-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="10ca2-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="10ca2-134">Este comando define um serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10ca2-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="10ca2-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="10ca2-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="10ca2-136">Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança.</span><span class="sxs-lookup"><span data-stu-id="10ca2-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="10ca2-137">O PowerShell ou o portal do Azure pode ser usado para configurar a sincronização neste servidor.</span><span class="sxs-lookup"><span data-stu-id="10ca2-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="10ca2-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="10ca2-139">Esse comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="10ca2-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="10ca2-140">Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade do servidor neste grupo de sincronização pode sincronizar.</span><span class="sxs-lookup"><span data-stu-id="10ca2-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="10ca2-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="10ca2-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="10ca2-142">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="10ca2-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="10ca2-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="10ca2-144">Esse comando excluirá o ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="10ca2-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="10ca2-145">A sincronização com este local será interrompida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="10ca2-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="10ca2-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="10ca2-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="10ca2-147">Esse comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="10ca2-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="10ca2-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="10ca2-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="10ca2-149">Use somente para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="10ca2-149">Use for troubleshooting only.</span></span> <span data-ttu-id="10ca2-150">Esse comando irá reverter o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ca2-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="10ca2-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10ca2-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="10ca2-152">Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="10ca2-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="10ca2-153">Cancelar registro-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="10ca2-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="10ca2-154">Aviso: o cancelamento do registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="10ca2-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="10ca2-155">Esse comando cancelará o registro de um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10ca2-155">This command will unregister a server from it's storage sync service.</span></span>

