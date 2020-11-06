---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: 66f7a4ced5c92aa6e6d9bc432f2aa3f6ebbde7e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431856"
---
# <span data-ttu-id="1506d-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1506d-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="1506d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1506d-102">SYNOPSIS</span></span>
<span data-ttu-id="1506d-103">Inicia a cópia de um blob.</span><span class="sxs-lookup"><span data-stu-id="1506d-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1506d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1506d-104">SYNTAX</span></span>

### <span data-ttu-id="1506d-105">ContainerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1506d-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="1506d-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-112">Instância</span><span class="sxs-lookup"><span data-stu-id="1506d-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="1506d-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1506d-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="1506d-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1506d-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1506d-115">DESCRIPTION</span></span>
<span data-ttu-id="1506d-116">O cmdlet **Start-AzureStorageBlobCopy** inicia a cópia de um blob.</span><span class="sxs-lookup"><span data-stu-id="1506d-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="1506d-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1506d-117">EXAMPLES</span></span>

### <span data-ttu-id="1506d-118">Exemplo 1: copiar um blob nomeado</span><span class="sxs-lookup"><span data-stu-id="1506d-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="1506d-119">Esse comando inicia a operação de cópia do blob chamado ContosoPlanning2015 do contêiner chamado ContosoUploads para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="1506d-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="1506d-120">Exemplo 2: obter um contêiner para especificar BLOBs a serem copiados</span><span class="sxs-lookup"><span data-stu-id="1506d-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="1506d-121">Esse comando obtém o contêiner chamado ContosoUploads, usando o cmdlet **Get-AzureStorageContainer** e, em seguida, passa o contêiner para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1506d-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1506d-122">Esse cmdlet inicia a operação de cópia do blob chamado ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="1506d-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="1506d-123">O cmdlet anterior fornece o contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="1506d-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="1506d-124">O parâmetro *DestContainer* especifica ContosoArchives como o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="1506d-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="1506d-125">Exemplo 3: obter um blob para copiar</span><span class="sxs-lookup"><span data-stu-id="1506d-125">Example 3: Get a blob to copy</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="1506d-126">Esse comando obtém os BLOBs no contêiner chamado ContosoUploads, usando o cmdlet **Get-AzureStorageBlob** e, em seguida, passa os resultados para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1506d-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1506d-127">Esse cmdlet inicia a operação de cópia dos BLOBs para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="1506d-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="1506d-128">Exemplo 4: copiar um blob especificado como um objeto</span><span class="sxs-lookup"><span data-stu-id="1506d-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="1506d-129">O primeiro comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="1506d-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="1506d-130">O comando armazena esse objeto na variável $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="1506d-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="1506d-131">O segundo comando obtém o blob chamado ContosoPlanning2015Archived no contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="1506d-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="1506d-132">O comando armazena esse objeto na variável $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="1506d-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="1506d-133">O último comando inicia a operação de cópia do contêiner de origem para o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="1506d-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="1506d-134">O comando usa notação de ponto padrão para especificar os objetos **ICloudBlob** para os blobs de $SrcBlob e $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="1506d-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="1506d-135">Exemplo 5: copiar um blob de um URI</span><span class="sxs-lookup"><span data-stu-id="1506d-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="1506d-136">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e armazena essa chave na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="1506d-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="1506d-137">O segundo comando copia o arquivo do URI especificado para o blob chamado ContosoPlanning no contêiner chamado ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="1506d-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="1506d-138">O comando inicia a operação de cópia no contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="1506d-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="1506d-139">OS</span><span class="sxs-lookup"><span data-stu-id="1506d-139">PARAMETERS</span></span>

### <span data-ttu-id="1506d-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="1506d-140">-AbsoluteUri</span></span>
<span data-ttu-id="1506d-141">Especifica o URI absoluto de um arquivo a ser copiado para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1506d-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1506d-143">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1506d-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1506d-144">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1506d-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1506d-145">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1506d-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-146">-CloudBlob</span></span>
<span data-ttu-id="1506d-147">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1506d-148">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="1506d-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1506d-149">-CloudBlobContainer</span></span>
<span data-ttu-id="1506d-150">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1506d-151">Esse cmdlet copia um blob do contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1506d-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="1506d-152">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="1506d-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1506d-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1506d-154">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1506d-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1506d-155">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1506d-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1506d-156">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1506d-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1506d-157">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1506d-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1506d-158">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1506d-158">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-159">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1506d-159">-Context</span></span>
<span data-ttu-id="1506d-160">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1506d-161">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1506d-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-162">-DestBlob</span></span>
<span data-ttu-id="1506d-163">Especifica o nome do blob de destino.</span><span class="sxs-lookup"><span data-stu-id="1506d-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-164">-DestCloudBlob</span></span>
<span data-ttu-id="1506d-165">Especifica um objeto **CloudBlob** de destino</span><span class="sxs-lookup"><span data-stu-id="1506d-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="1506d-166">-DestContainer</span></span>
<span data-ttu-id="1506d-167">Especifica o nome do contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="1506d-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="1506d-168">-DestContext</span></span>
<span data-ttu-id="1506d-169">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1506d-170">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1506d-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-171">-Force</span><span class="sxs-lookup"><span data-stu-id="1506d-171">-Force</span></span>
<span data-ttu-id="1506d-172">Indica que esse cmdlet substitui o blob de destino sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="1506d-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="1506d-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="1506d-174">Camada de BLOB da página Premium</span><span class="sxs-lookup"><span data-stu-id="1506d-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1506d-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1506d-176">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1506d-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1506d-177">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1506d-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-178">-SrcBlob</span></span>
<span data-ttu-id="1506d-179">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="1506d-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="1506d-180">-SrcContainer</span></span>
<span data-ttu-id="1506d-181">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="1506d-181">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="1506d-182">-SrcDir</span></span>
<span data-ttu-id="1506d-183">Especifica um objeto **CloudFileDirectory** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="1506d-184">-SrcFile</span></span>
<span data-ttu-id="1506d-185">Especifica um objeto **cloudfile** da biblioteca do Azure Storage Client.</span><span class="sxs-lookup"><span data-stu-id="1506d-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1506d-186">Você pode criá-lo ou usar Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1506d-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="1506d-187">-SrcFilePath</span></span>
<span data-ttu-id="1506d-188">Especifica o caminho relativo do arquivo de origem do diretório de origem ou do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="1506d-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="1506d-189">-SrcShare</span></span>
<span data-ttu-id="1506d-190">Especifica um objeto **CloudFileShare** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1506d-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1506d-191">Você pode criá-lo ou usar Get-AzureStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1506d-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-192">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="1506d-192">-SrcShareName</span></span>
<span data-ttu-id="1506d-193">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="1506d-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1506d-194">-Confirm</span></span>
<span data-ttu-id="1506d-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1506d-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1506d-196">-WhatIf</span></span>
<span data-ttu-id="1506d-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1506d-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1506d-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1506d-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1506d-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1506d-199">CommonParameters</span></span>
<span data-ttu-id="1506d-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1506d-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1506d-201">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1506d-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1506d-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1506d-202">INPUTS</span></span>

### <span data-ttu-id="1506d-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-203">CloudBlob</span></span>

<span data-ttu-id="1506d-204">O parâmetro ' CloudBlob ' aceita o valor do tipo ' CloudBlob ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1506d-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="1506d-205">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1506d-205">IStorageContext</span></span>

<span data-ttu-id="1506d-206">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1506d-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1506d-207">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1506d-207">IStorageContext</span></span>

<span data-ttu-id="1506d-208">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1506d-208">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1506d-209">Cloudfile</span><span class="sxs-lookup"><span data-stu-id="1506d-209">CloudFile</span></span>

<span data-ttu-id="1506d-210">O parâmetro ' SrcFile ' aceita o valor do tipo ' Cloudfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1506d-210">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="1506d-211">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1506d-211">OUTPUTS</span></span>

### <span data-ttu-id="1506d-212">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1506d-212">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1506d-213">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1506d-213">NOTES</span></span>

## <span data-ttu-id="1506d-214">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1506d-214">RELATED LINKS</span></span>

[<span data-ttu-id="1506d-215">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="1506d-215">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="1506d-216">Parar-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1506d-216">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)