---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 36ae8a00237be287262de0cc9eac4022b9efc9d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941504"
---
# <span data-ttu-id="cc5c4-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cc5c4-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="cc5c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5c4-103">Inicia a cópia de um blob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="cc5c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc5c4-104">SYNTAX</span></span>

### <span data-ttu-id="cc5c4-105">ContainerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc5c4-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="cc5c4-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-112">Instância</span><span class="sxs-lookup"><span data-stu-id="cc5c4-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="cc5c4-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc5c4-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="cc5c4-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc5c4-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc5c4-115">DESCRIPTION</span></span>
<span data-ttu-id="cc5c4-116">O cmdlet **Start-AzStorageBlobCopy** inicia a cópia de um blob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="cc5c4-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc5c4-117">EXAMPLES</span></span>

### <span data-ttu-id="cc5c4-118">Exemplo 1: copiar um blob nomeado</span><span class="sxs-lookup"><span data-stu-id="cc5c4-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="cc5c4-119">Esse comando inicia a operação de cópia do blob chamado ContosoPlanning2015 do contêiner chamado ContosoUploads para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="cc5c4-120">Exemplo 2: obter um contêiner para especificar BLOBs a serem copiados</span><span class="sxs-lookup"><span data-stu-id="cc5c4-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="cc5c4-121">Esse comando obtém o contêiner chamado ContosoUploads, usando o cmdlet **Get-AzStorageContainer** e, em seguida, passa o contêiner para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cc5c4-122">Esse cmdlet inicia a operação de cópia do blob chamado ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="cc5c4-123">O cmdlet anterior fornece o contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="cc5c4-124">O parâmetro *DestContainer* especifica ContosoArchives como o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="cc5c4-125">Exemplo 3: obter todos os BLOBs em um contêiner e copiá-los</span><span class="sxs-lookup"><span data-stu-id="cc5c4-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="cc5c4-126">Esse comando obtém os BLOBs no contêiner chamado ContosoUploads, usando o cmdlet **Get-AzStorageBlob** e, em seguida, passa os resultados para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cc5c4-127">Esse cmdlet inicia a operação de cópia dos BLOBs para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="cc5c4-128">Exemplo 4: copiar um blob especificado como um objeto</span><span class="sxs-lookup"><span data-stu-id="cc5c4-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="cc5c4-129">O primeiro comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="cc5c4-130">O comando armazena esse objeto na variável $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="cc5c4-131">O segundo comando obtém o blob chamado ContosoPlanning2015Archived no contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="cc5c4-132">O comando armazena esse objeto na variável $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="cc5c4-133">O último comando inicia a operação de cópia do contêiner de origem para o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="cc5c4-134">O comando usa notação de ponto padrão para especificar os objetos **ICloudBlob** para os blobs de $SrcBlob e $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="cc5c4-135">Exemplo 5: copiar um blob de um URI</span><span class="sxs-lookup"><span data-stu-id="cc5c4-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="cc5c4-136">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e armazena essa chave na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="cc5c4-137">O segundo comando copia o arquivo do URI especificado para o blob chamado ContosoPlanning no contêiner chamado ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="cc5c4-138">O comando inicia a operação de cópia no contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="cc5c4-139">Exemplo 6: copiar um blob de bloco para o contêiner de destino com um novo nome de BLOB e definir blob de StandardBlobTier como Hot, RehydratePriority as High</span><span class="sxs-lookup"><span data-stu-id="cc5c4-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="cc5c4-140">Esse comando inicia a operação de cópia de um blob de bloco para contêiner de destino com um novo nome de BLOB e define o blob de destino StandardBlobTier como Hot, RehydratePriority as High</span><span class="sxs-lookup"><span data-stu-id="cc5c4-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="cc5c4-141">OS</span><span class="sxs-lookup"><span data-stu-id="cc5c4-141">PARAMETERS</span></span>

### <span data-ttu-id="cc5c4-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="cc5c4-142">-AbsoluteUri</span></span>
<span data-ttu-id="cc5c4-143">Especifica o URI absoluto de um arquivo a ser copiado para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="cc5c4-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc5c4-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cc5c4-145">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cc5c4-146">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cc5c4-147">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-148">-CloudBlob</span></span>
<span data-ttu-id="cc5c4-149">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc5c4-150">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cc5c4-151">-CloudBlobContainer</span></span>
<span data-ttu-id="cc5c4-152">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="cc5c4-153">Esse cmdlet copia um blob do contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="cc5c4-154">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cc5c4-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cc5c4-156">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cc5c4-157">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cc5c4-158">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cc5c4-159">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cc5c4-160">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-160">The default value is 10.</span></span>

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

### <span data-ttu-id="cc5c4-161">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cc5c4-161">-Context</span></span>
<span data-ttu-id="cc5c4-162">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc5c4-163">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="cc5c4-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5c4-164">-DefaultProfile</span></span>
<span data-ttu-id="cc5c4-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5c4-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-166">-DestBlob</span></span>
<span data-ttu-id="cc5c4-167">Especifica o nome do blob de destino.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-167">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="cc5c4-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-168">-DestCloudBlob</span></span>
<span data-ttu-id="cc5c4-169">Especifica um objeto **CloudBlob** de destino</span><span class="sxs-lookup"><span data-stu-id="cc5c4-169">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="cc5c4-170">-DestContainer</span></span>
<span data-ttu-id="cc5c4-171">Especifica o nome do contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-171">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="cc5c4-172">-DestContext</span></span>
<span data-ttu-id="cc5c4-173">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc5c4-174">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cc5c4-175">-Force</span><span class="sxs-lookup"><span data-stu-id="cc5c4-175">-Force</span></span>
<span data-ttu-id="cc5c4-176">Indica que esse cmdlet substitui o blob de destino sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cc5c4-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="cc5c4-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="cc5c4-178">Camada de BLOB da página Premium</span><span class="sxs-lookup"><span data-stu-id="cc5c4-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="cc5c4-179">-RehydratePriority</span></span>
<span data-ttu-id="cc5c4-180">Bloquear blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="cc5c4-181">Indica a prioridade com a qual rehydrate um blob arquivado.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="cc5c4-182">Os valores válidos são High/Standard.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc5c4-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cc5c4-184">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cc5c4-185">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-186">-SrcBlob</span></span>
<span data-ttu-id="cc5c4-187">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-187">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="cc5c4-188">-SrcContainer</span></span>
<span data-ttu-id="cc5c4-189">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="cc5c4-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="cc5c4-190">-SrcDir</span></span>
<span data-ttu-id="cc5c4-191">Especifica um objeto **CloudFileDirectory** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="cc5c4-192">-SrcFile</span></span>
<span data-ttu-id="cc5c4-193">Especifica um objeto **cloudfile** da biblioteca do Azure Storage Client.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc5c4-194">Você pode criá-lo ou usar Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="cc5c4-195">-SrcFilePath</span></span>
<span data-ttu-id="cc5c4-196">Especifica o caminho relativo do arquivo de origem do diretório de origem ou do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-196">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="cc5c4-197">-SrcShare</span></span>
<span data-ttu-id="cc5c4-198">Especifica um objeto **CloudFileShare** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="cc5c4-199">Você pode criá-lo ou usar Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="cc5c4-200">-SrcShareName</span></span>
<span data-ttu-id="cc5c4-201">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-201">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="cc5c4-202">-StandardBlobTier</span></span>
<span data-ttu-id="cc5c4-203">Camada de bloco de BLOB, os valores válidos são quente/interessante/arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="cc5c4-204">Veja detalhes em https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="cc5c4-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="cc5c4-205">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc5c4-205">-Confirm</span></span>
<span data-ttu-id="cc5c4-206">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-206">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5c4-207">-WhatIf</span></span>
<span data-ttu-id="cc5c4-208">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5c4-209">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-209">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5c4-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5c4-210">CommonParameters</span></span>
<span data-ttu-id="cc5c4-211">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5c4-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5c4-212">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5c4-212">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5c4-213">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc5c4-213">INPUTS</span></span>

### <span data-ttu-id="cc5c4-214">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cc5c4-215">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cc5c4-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cc5c4-216">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="cc5c4-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cc5c4-217">System. String</span><span class="sxs-lookup"><span data-stu-id="cc5c4-217">System.String</span></span>

### <span data-ttu-id="cc5c4-218">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc5c4-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cc5c4-219">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc5c4-219">OUTPUTS</span></span>

### <span data-ttu-id="cc5c4-220">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cc5c4-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cc5c4-221">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc5c4-221">NOTES</span></span>

## <span data-ttu-id="cc5c4-222">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc5c4-222">RELATED LINKS</span></span>

[<span data-ttu-id="cc5c4-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="cc5c4-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="cc5c4-224">Parar-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cc5c4-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
