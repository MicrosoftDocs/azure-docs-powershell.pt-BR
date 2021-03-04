---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888033"
---
# <span data-ttu-id="20ef2-101">Módulo Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="20ef2-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="20ef2-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="20ef2-102">Description</span></span>
<span data-ttu-id="20ef2-103">Os cmdlets no módulo de Sincronização de Armazenamento permitem gerenciar operações relacionadas à Sincronização de Arquivos do Azure no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20ef2-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="20ef2-104">Az.StorageSync Cmdlets</span><span class="sxs-lookup"><span data-stu-id="20ef2-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="20ef2-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20ef2-106">Este comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="20ef2-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="20ef2-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20ef2-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="20ef2-108">Este comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20ef2-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="20ef2-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20ef2-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="20ef2-110">Este comando lista todos os servidores registrados em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20ef2-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="20ef2-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20ef2-112">Este comando lista todos os pontos de extremidade do servidor em um determinado grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="20ef2-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="20ef2-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20ef2-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="20ef2-114">Este comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de assinatura/recurso.</span><span class="sxs-lookup"><span data-stu-id="20ef2-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="20ef2-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="20ef2-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="20ef2-116">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="20ef2-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="20ef2-117">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="20ef2-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="20ef2-118">No máximo 10.000 alterações podem ser detectadas.</span><span class="sxs-lookup"><span data-stu-id="20ef2-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="20ef2-119">Se o escopo das alterações for conhecido para você, limite a execução deste comando a partes do namespace, para que a detecção de alterações possa ser finalização rápida e dentro de um limite de 10.000 alterações.</span><span class="sxs-lookup"><span data-stu-id="20ef2-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="20ef2-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="20ef2-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="20ef2-121">Verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="20ef2-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="20ef2-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="20ef2-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="20ef2-123">Este comando relembra todos os arquivos hierárquiquios de volta para o disco local.</span><span class="sxs-lookup"><span data-stu-id="20ef2-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="20ef2-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20ef2-125">Este comando cria um ponto de extremidade de nuvem de sincronização de arquivos do Azure em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="20ef2-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="20ef2-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20ef2-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="20ef2-127">Este comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="20ef2-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="20ef2-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20ef2-129">Este comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="20ef2-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="20ef2-130">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="20ef2-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="20ef2-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20ef2-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="20ef2-132">Este comando cria um novo serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20ef2-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="20ef2-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20ef2-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="20ef2-134">Este comando define um serviço de sincronização de armazenamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20ef2-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="20ef2-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20ef2-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="20ef2-136">Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança.</span><span class="sxs-lookup"><span data-stu-id="20ef2-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="20ef2-137">O PowerShell ou o portal do Azure podem ser usados para configurar a sincronização neste servidor.</span><span class="sxs-lookup"><span data-stu-id="20ef2-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="20ef2-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20ef2-139">Este comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="20ef2-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="20ef2-140">Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade de servidor neste grupo de sincronização pode sincronizar.</span><span class="sxs-lookup"><span data-stu-id="20ef2-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="20ef2-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20ef2-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="20ef2-142">Este comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="20ef2-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="20ef2-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20ef2-144">Este comando excluirá o ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="20ef2-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="20ef2-145">A sincronização com esse local será parada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="20ef2-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="20ef2-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20ef2-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="20ef2-147">Este comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="20ef2-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="20ef2-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="20ef2-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="20ef2-149">Use apenas para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="20ef2-149">Use for troubleshooting only.</span></span> <span data-ttu-id="20ef2-150">Esse comando rolará o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20ef2-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="20ef2-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ef2-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20ef2-152">Este comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="20ef2-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="20ef2-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20ef2-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="20ef2-154">Aviso: o não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor.</span><span class="sxs-lookup"><span data-stu-id="20ef2-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="20ef2-155">Esse comando desacreva um servidor do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20ef2-155">This command will unregister a server from it's storage sync service.</span></span>

