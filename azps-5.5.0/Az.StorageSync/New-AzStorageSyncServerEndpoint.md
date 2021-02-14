---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115633"
---
# <span data-ttu-id="4de6d-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4de6d-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4de6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4de6d-102">SYNOPSIS</span></span>
<span data-ttu-id="4de6d-103">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="4de6d-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="4de6d-104">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4de6d-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="4de6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4de6d-105">SYNTAX</span></span>

### <span data-ttu-id="4de6d-106">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4de6d-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de6d-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de6d-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de6d-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de6d-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de6d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4de6d-109">DESCRIPTION</span></span>
<span data-ttu-id="4de6d-110">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="4de6d-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="4de6d-111">Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4de6d-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="4de6d-112">Se já houver arquivos em outros pontos de extremidade no grupo de sincronização e esse local recém-adicionado também contiver arquivos, um processo de reconciliação tentará determinar se os arquivos são realmente os mesmos nas mesmas pastas que em outros pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="4de6d-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="4de6d-113">Os namespaces mesclam e a reconciliação ajuda a evitar arquivos de conflito.</span><span class="sxs-lookup"><span data-stu-id="4de6d-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="4de6d-114">Se houver arquivos em outros pontos de extremidade do servidor, é geralmente melhor começar com um local vazio neste servidor, para que os arquivos da nuvem sejam baixados para o servidor em um processo automático chamado recuperação rápida de desastres.</span><span class="sxs-lookup"><span data-stu-id="4de6d-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="4de6d-115">Os metadados de namespace serão sincronizados primeiro e, em seguida, o fluxo de dados de cada arquivo será baixado.</span><span class="sxs-lookup"><span data-stu-id="4de6d-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="4de6d-116">Se um arquivo for solicitado por um usuário ou aplicativo fora da ordem de download, esse arquivo será chamado com prioridade para atender à solicitação de acesso.</span><span class="sxs-lookup"><span data-stu-id="4de6d-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="4de6d-117">Opcionalmente, você pode usar a camada de nuvem neste ponto de extremidade do servidor para determinar se esse ponto de extremidade deve se tornar um cache do conjunto completo de arquivos da nuvem.</span><span class="sxs-lookup"><span data-stu-id="4de6d-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="4de6d-118">Se a camada de nuvem for usada, o download de conteúdo de arquivo será parar no ponto definido pelas políticas de camadas de nuvem que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="4de6d-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="4de6d-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4de6d-119">EXAMPLES</span></span>

### <span data-ttu-id="4de6d-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4de6d-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="4de6d-121">Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado e o insere em um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4de6d-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="4de6d-122">Sua maneira de fazer parte de uma topologia de outros pontos de extremidade, metadados de arquivo e conteúdo começará imediatamente a sincronizar entre todos os locais referenciados como pontos de extremidade no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4de6d-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="4de6d-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4de6d-123">PARAMETERS</span></span>

### <span data-ttu-id="4de6d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4de6d-124">-AsJob</span></span>
<span data-ttu-id="4de6d-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4de6d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4de6d-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="4de6d-126">-CloudTiering</span></span>
<span data-ttu-id="4de6d-127">Parâmetro de camada de nuvem</span><span class="sxs-lookup"><span data-stu-id="4de6d-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="4de6d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de6d-128">-DefaultProfile</span></span>
<span data-ttu-id="4de6d-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4de6d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de6d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4de6d-130">-Name</span></span>
<span data-ttu-id="4de6d-131">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4de6d-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="4de6d-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="4de6d-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="4de6d-133">Parâmetro de Dados de Seeded na Nuvem</span><span class="sxs-lookup"><span data-stu-id="4de6d-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="4de6d-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="4de6d-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="4de6d-135">Parâmetro Uri do Compartilhamento de Arquivos de Seeded na Nuvem</span><span class="sxs-lookup"><span data-stu-id="4de6d-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="4de6d-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="4de6d-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="4de6d-137">Parâmetro do modo de cache local</span><span class="sxs-lookup"><span data-stu-id="4de6d-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="4de6d-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="4de6d-138">-localCacheMode</span></span>
<span data-ttu-id="4de6d-139">Parâmetro do modo de cache local</span><span class="sxs-lookup"><span data-stu-id="4de6d-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="4de6d-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4de6d-140">-ParentObject</span></span>
<span data-ttu-id="4de6d-141">Objeto SyncGroup, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4de6d-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="4de6d-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4de6d-142">-ParentResourceId</span></span>
<span data-ttu-id="4de6d-143">ID do Recurso Pai do SyncGroup</span><span class="sxs-lookup"><span data-stu-id="4de6d-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="4de6d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de6d-144">-ResourceGroupName</span></span>
<span data-ttu-id="4de6d-145">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4de6d-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="4de6d-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="4de6d-146">-ServerLocalPath</span></span>
<span data-ttu-id="4de6d-147">Parâmetro de Caminho Local do Servidor</span><span class="sxs-lookup"><span data-stu-id="4de6d-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="4de6d-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="4de6d-148">-ServerResourceId</span></span>
<span data-ttu-id="4de6d-149">ID do Recurso RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="4de6d-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="4de6d-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4de6d-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="4de6d-151">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4de6d-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4de6d-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4de6d-152">-SyncGroupName</span></span>
<span data-ttu-id="4de6d-153">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4de6d-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4de6d-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4de6d-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="4de6d-155">Parâmetro Arquivos de Camada Mais Antigos que Dias</span><span class="sxs-lookup"><span data-stu-id="4de6d-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="4de6d-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4de6d-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="4de6d-157">Parâmetro porcentagem de espaço livre de volume</span><span class="sxs-lookup"><span data-stu-id="4de6d-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="4de6d-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4de6d-158">-Confirm</span></span>
<span data-ttu-id="4de6d-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de6d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de6d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de6d-160">-WhatIf</span></span>
<span data-ttu-id="4de6d-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4de6d-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4de6d-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4de6d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de6d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de6d-163">CommonParameters</span></span>
<span data-ttu-id="4de6d-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de6d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de6d-165">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de6d-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de6d-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="4de6d-166">INPUTS</span></span>

### <span data-ttu-id="4de6d-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4de6d-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="4de6d-168">System.String</span><span class="sxs-lookup"><span data-stu-id="4de6d-168">System.String</span></span>

## <span data-ttu-id="4de6d-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="4de6d-169">OUTPUTS</span></span>

### <span data-ttu-id="4de6d-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4de6d-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4de6d-171">Notas</span><span class="sxs-lookup"><span data-stu-id="4de6d-171">NOTES</span></span>

## <span data-ttu-id="4de6d-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de6d-172">RELATED LINKS</span></span>
