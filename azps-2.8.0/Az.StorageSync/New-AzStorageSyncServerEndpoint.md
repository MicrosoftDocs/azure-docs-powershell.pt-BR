---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 524e9334b3e706dc51a2dfd4efc5d6f3cce710c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774312"
---
# <span data-ttu-id="a0f72-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0f72-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="a0f72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0f72-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f72-103">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="a0f72-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="a0f72-104">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a0f72-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="a0f72-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f72-105">SYNTAX</span></span>

### <span data-ttu-id="a0f72-106">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0f72-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f72-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="a0f72-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f72-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f72-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f72-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0f72-109">DESCRIPTION</span></span>
<span data-ttu-id="a0f72-110">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="a0f72-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="a0f72-111">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a0f72-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="a0f72-112">Se houver arquivos em outros pontos de extremidade no grupo de sincronização e esse local recém-adicionado também contiver arquivos, um processo de reconciliação tentará determinar se os arquivos são, na verdade, os mesmos nas mesmas pastas que em outros pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a0f72-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="a0f72-113">Os namespaces serão mesclados e a reconciliação ajudará a evitar arquivos de conflito.</span><span class="sxs-lookup"><span data-stu-id="a0f72-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="a0f72-114">Se houver arquivos em outros pontos de extremidade do servidor, muitas vezes é melhor começar com um local vazio neste servidor, de modo que os arquivos da nuvem sejam inseridos no servidor em um processo automático chamado recuperação rápida de desastres.</span><span class="sxs-lookup"><span data-stu-id="a0f72-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="a0f72-115">Os metadados de namespace serão sincronizados primeiro, e o fluxo de dados de cada arquivo será baixado.</span><span class="sxs-lookup"><span data-stu-id="a0f72-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="a0f72-116">Se um arquivo for solicitado por um usuário ou aplicativo fora da ordem de download, esse arquivo será cancelado com prioridade para atender à solicitação de acesso.</span><span class="sxs-lookup"><span data-stu-id="a0f72-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="a0f72-117">Opcionalmente, você pode usar a hierarquização na nuvem nesse ponto de extremidade do servidor para determinar se esse ponto de extremidade deve se tornar um cache do conjunto completo de arquivos da nuvem.</span><span class="sxs-lookup"><span data-stu-id="a0f72-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="a0f72-118">Se a camada de nuvem for usada, o download do conteúdo do arquivo será interrompido no ponto definido pelas políticas de camada de nuvem que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="a0f72-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="a0f72-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0f72-119">EXAMPLES</span></span>

### <span data-ttu-id="a0f72-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0f72-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="a0f72-121">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado e o insere em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a0f72-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="a0f72-122">Dessa forma, ele faz parte de uma topologia de outros pontos de extremidade, e os metadados e o conteúdo do arquivo serão iniciados imediatamente na sincronização entre todos os locais mencionados como pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a0f72-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="a0f72-123">OS</span><span class="sxs-lookup"><span data-stu-id="a0f72-123">PARAMETERS</span></span>

### <span data-ttu-id="a0f72-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0f72-124">-AsJob</span></span>
<span data-ttu-id="a0f72-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a0f72-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="a0f72-126">-CloudTiering</span></span>
<span data-ttu-id="a0f72-127">Parâmetro de hierarquização na nuvem</span><span class="sxs-lookup"><span data-stu-id="a0f72-127">Cloud Tiering Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f72-128">-DefaultProfile</span></span>
<span data-ttu-id="a0f72-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f72-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0f72-130">-Name</span></span>
<span data-ttu-id="a0f72-131">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a0f72-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="a0f72-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="a0f72-133">Parâmetro de dados propagados na nuvem</span><span class="sxs-lookup"><span data-stu-id="a0f72-133">Cloud Seeded Data Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="a0f72-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="a0f72-135">Parâmetro de URI do compartilhamento de arquivo de dados propagados na nuvem</span><span class="sxs-lookup"><span data-stu-id="a0f72-135">Cloud Seeded Data File Share Uri Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a0f72-136">-ParentObject</span></span>
<span data-ttu-id="a0f72-137">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a0f72-137">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f72-138">-ParentResourceId</span></span>
<span data-ttu-id="a0f72-139">ID do recurso pai do pool de sincronização</span><span class="sxs-lookup"><span data-stu-id="a0f72-139">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f72-140">-ResourceGroupName</span></span>
<span data-ttu-id="a0f72-141">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0f72-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="a0f72-142">-ServerLocalPath</span></span>
<span data-ttu-id="a0f72-143">Parâmetro de caminho local do servidor</span><span class="sxs-lookup"><span data-stu-id="a0f72-143">Server Local Path Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f72-144">-ServerResourceId</span></span>
<span data-ttu-id="a0f72-145">ID do recurso de RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="a0f72-145">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a0f72-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="a0f72-147">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a0f72-147">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f72-148">-SyncGroupName</span></span>
<span data-ttu-id="a0f72-149">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="a0f72-149">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="a0f72-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="a0f72-151">O parâmetro arquivos de camada com mais de dias</span><span class="sxs-lookup"><span data-stu-id="a0f72-151">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="a0f72-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="a0f72-153">Parâmetro de porcentagem do espaço livre no volume</span><span class="sxs-lookup"><span data-stu-id="a0f72-153">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0f72-154">-Confirm</span></span>
<span data-ttu-id="a0f72-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f72-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f72-156">-WhatIf</span></span>
<span data-ttu-id="a0f72-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0f72-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0f72-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0f72-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f72-159">CommonParameters</span></span>
<span data-ttu-id="a0f72-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f72-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f72-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f72-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f72-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0f72-162">INPUTS</span></span>

### <span data-ttu-id="a0f72-163">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a0f72-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="a0f72-164">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f72-164">System.String</span></span>

## <span data-ttu-id="a0f72-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0f72-165">OUTPUTS</span></span>

### <span data-ttu-id="a0f72-166">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0f72-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a0f72-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0f72-167">NOTES</span></span>

## <span data-ttu-id="a0f72-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0f72-168">RELATED LINKS</span></span>