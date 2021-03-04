---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890059"
---
# <span data-ttu-id="e1c9b-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="e1c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c9b-103">Copie um blob de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="e1c9b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1c9b-104">SYNTAX</span></span>

### <span data-ttu-id="e1c9b-105">ContainerName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1c9b-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c9b-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="e1c9b-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c9b-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="e1c9b-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c9b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1c9b-108">DESCRIPTION</span></span>
<span data-ttu-id="e1c9b-109">O cmdlet **Copy-AzStorageBlob** copia um blob de forma síncrona, atualmente só suporta blob de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="e1c9b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-110">EXAMPLES</span></span>

### <span data-ttu-id="e1c9b-111">Exemplo 1: copiar um blob nomeado para outro</span><span class="sxs-lookup"><span data-stu-id="e1c9b-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="e1c9b-112">Este comando copia um blob do contêiner de origem para o contêiner de destino com um novo nome de blob.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="e1c9b-113">Exemplo 2: Copiar blob de um objeto blob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="e1c9b-114">Este comando copia um blob do objeto blob de origem para o contêiner de destino com um novo nome de blob.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="e1c9b-115">Exemplo 3: Copiar blob de um Uri blob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="e1c9b-116">O primeiro comando cria um Uri blob do blob de origem, com sas token de permissão "rt".</span><span class="sxs-lookup"><span data-stu-id="e1c9b-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="e1c9b-117">O segundo comando copia do blob de origem Uri para o blob de destino.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="e1c9b-118">Exemplo 4: atualizar um escopo de criptografia de blob bloqueado</span><span class="sxs-lookup"><span data-stu-id="e1c9b-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="e1c9b-119">Este comando atualiza um escopo de criptografia blob de bloqueio copiando-o para si mesmo com um novo escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="e1c9b-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-120">PARAMETERS</span></span>

### <span data-ttu-id="e1c9b-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="e1c9b-121">-AbsoluteUri</span></span>
<span data-ttu-id="e1c9b-122">uri de blob de origem</span><span class="sxs-lookup"><span data-stu-id="e1c9b-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-123">-AsJob</span></span>
<span data-ttu-id="e1c9b-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e1c9b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1c9b-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e1c9b-125">-BlobBaseClient</span></span>
<span data-ttu-id="e1c9b-126">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e1c9b-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e1c9b-127">-Context</span></span>
<span data-ttu-id="e1c9b-128">Objeto de contexto de armazenamento de origem do Azure</span><span class="sxs-lookup"><span data-stu-id="e1c9b-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c9b-129">-DefaultProfile</span></span>
<span data-ttu-id="e1c9b-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-131">-DestBlob</span></span>
<span data-ttu-id="e1c9b-132">Nome do blob de destino</span><span class="sxs-lookup"><span data-stu-id="e1c9b-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="e1c9b-133">-DestContainer</span></span>
<span data-ttu-id="e1c9b-134">Nome do contêiner de destino</span><span class="sxs-lookup"><span data-stu-id="e1c9b-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="e1c9b-135">-DestContext</span></span>
<span data-ttu-id="e1c9b-136">Objeto de contexto de armazenamento de destino</span><span class="sxs-lookup"><span data-stu-id="e1c9b-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e1c9b-137">-EncryptionScope</span></span>
<span data-ttu-id="e1c9b-138">Escopo de criptografia a ser usado ao fazer solicitações ao blob dest.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="e1c9b-139">-Force</span><span class="sxs-lookup"><span data-stu-id="e1c9b-139">-Force</span></span>
<span data-ttu-id="e1c9b-140">Forçar a substituir o blob ou o arquivo existente</span><span class="sxs-lookup"><span data-stu-id="e1c9b-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="e1c9b-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="e1c9b-141">-RehydratePriority</span></span>
<span data-ttu-id="e1c9b-142">Bloquear Blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="e1c9b-143">Indica a prioridade com a qual reidratar um blob arquivado.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="e1c9b-144">Os valores válidos são High/Standard.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-145">-SrcBlob</span></span>
<span data-ttu-id="e1c9b-146">Nome de blob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="e1c9b-147">-SrcContainer</span></span>
<span data-ttu-id="e1c9b-148">Nome do contêiner de origem</span><span class="sxs-lookup"><span data-stu-id="e1c9b-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="e1c9b-149">-StandardBlobTier</span></span>
<span data-ttu-id="e1c9b-150">Bloquear Camada de Blob, os valores válidos são Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="e1c9b-151">Confira detalhes em https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="e1c9b-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c9b-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c9b-152">-Confirm</span></span>
<span data-ttu-id="e1c9b-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c9b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c9b-154">-WhatIf</span></span>
<span data-ttu-id="e1c9b-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c9b-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c9b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c9b-157">CommonParameters</span></span>
<span data-ttu-id="e1c9b-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c9b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c9b-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c9b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c9b-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-160">INPUTS</span></span>

### <span data-ttu-id="e1c9b-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e1c9b-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="e1c9b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="e1c9b-162">System.String</span></span>

### <span data-ttu-id="e1c9b-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1c9b-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1c9b-164">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-164">OUTPUTS</span></span>

### <span data-ttu-id="e1c9b-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e1c9b-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="e1c9b-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1c9b-166">NOTES</span></span>

## <span data-ttu-id="e1c9b-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1c9b-167">RELATED LINKS</span></span>
