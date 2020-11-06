---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425424"
---
# <span data-ttu-id="99f7f-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="99f7f-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="99f7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="99f7f-103">Iniciar uma operação de cópia incremental de um instantâneo de blob de página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="99f7f-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="99f7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f7f-104">SYNTAX</span></span>

### <span data-ttu-id="99f7f-105">ContainerInstance (padrão)</span><span class="sxs-lookup"><span data-stu-id="99f7f-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99f7f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="99f7f-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99f7f-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="99f7f-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99f7f-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="99f7f-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99f7f-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="99f7f-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="99f7f-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99f7f-110">DESCRIPTION</span></span>
<span data-ttu-id="99f7f-111">Iniciar uma operação de cópia incremental de um instantâneo de blob de página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="99f7f-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="99f7f-112">Veja mais detalhes do recurso em https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="99f7f-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="99f7f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99f7f-113">EXAMPLES</span></span>

### <span data-ttu-id="99f7f-114">Exemplo 1: iniciar a operação de cópia incremental por nome do blob e tempo do instantâneo</span><span class="sxs-lookup"><span data-stu-id="99f7f-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="99f7f-115">Este comando inicia a operação de cópia incremental por nome do blob e tempo do instantâneo</span><span class="sxs-lookup"><span data-stu-id="99f7f-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="99f7f-116">Exemplo 2: iniciar a operação de cópia incremental usando o URI de origem</span><span class="sxs-lookup"><span data-stu-id="99f7f-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="99f7f-117">Este comando inicia a operação de cópia incremental usando o URI de origem</span><span class="sxs-lookup"><span data-stu-id="99f7f-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="99f7f-118">Exemplo 3: iniciar a operação de cópia incremental usando o pipeline de contêiner de GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="99f7f-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="99f7f-119">Este comando inicia a operação de cópia incremental usando o pipeline de contêiner do GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="99f7f-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="99f7f-120">Exemplo 4: iniciar a operação de cópia incremental do objeto CloudPageBlob para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="99f7f-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="99f7f-121">Este comando inicia a operação de cópia incremental do objeto CloudPageBlob para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="99f7f-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="99f7f-122">OS</span><span class="sxs-lookup"><span data-stu-id="99f7f-122">PARAMETERS</span></span>

### <span data-ttu-id="99f7f-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="99f7f-123">-AbsoluteUri</span></span>
<span data-ttu-id="99f7f-124">URI absoluto para a fonte.</span><span class="sxs-lookup"><span data-stu-id="99f7f-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="99f7f-125">Lembre-se de que a credencial deve ser fornecida no URI, se a origem exigir algum.</span><span class="sxs-lookup"><span data-stu-id="99f7f-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="99f7f-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="99f7f-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="99f7f-127">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="99f7f-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="99f7f-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-128">-CloudBlob</span></span>
<span data-ttu-id="99f7f-129">Objeto CloudBlob da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="99f7f-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="99f7f-130">Você pode criá-lo ou usar Get-AzureStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f7f-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99f7f-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="99f7f-131">-CloudBlobContainer</span></span>
<span data-ttu-id="99f7f-132">Objeto CloudBlobContainer da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="99f7f-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="99f7f-133">Você pode criá-lo ou usar Get-AzureStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f7f-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="99f7f-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="99f7f-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="99f7f-135">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="99f7f-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="99f7f-136">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="99f7f-136">The default value is 10.</span></span>

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

### <span data-ttu-id="99f7f-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="99f7f-137">-Context</span></span>
<span data-ttu-id="99f7f-138">Contexto de armazenamento do Azure de origem.</span><span class="sxs-lookup"><span data-stu-id="99f7f-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="99f7f-139">Você pode criá-lo por New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f7f-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="99f7f-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-140">-DestBlob</span></span>
<span data-ttu-id="99f7f-141">Nome do blob de destino</span><span class="sxs-lookup"><span data-stu-id="99f7f-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="99f7f-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-142">-DestCloudBlob</span></span>
<span data-ttu-id="99f7f-143">Objeto CloudBlob de destino</span><span class="sxs-lookup"><span data-stu-id="99f7f-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f7f-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="99f7f-144">-DestContainer</span></span>
<span data-ttu-id="99f7f-145">Nome do contêiner de destino</span><span class="sxs-lookup"><span data-stu-id="99f7f-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f7f-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="99f7f-146">-DestContext</span></span>
<span data-ttu-id="99f7f-147">Contexto de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="99f7f-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="99f7f-148">Você pode criá-lo por New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f7f-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="99f7f-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="99f7f-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="99f7f-150">O tempo limite do servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="99f7f-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="99f7f-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-151">-SrcBlob</span></span>
<span data-ttu-id="99f7f-152">Nome do blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="99f7f-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f7f-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="99f7f-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="99f7f-154">Tempo de instantâneo do blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="99f7f-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f7f-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="99f7f-155">-SrcContainer</span></span>
<span data-ttu-id="99f7f-156">Nome do contêiner de origem</span><span class="sxs-lookup"><span data-stu-id="99f7f-156">Source Container name</span></span>

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

### <span data-ttu-id="99f7f-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99f7f-157">-Confirm</span></span>
<span data-ttu-id="99f7f-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f7f-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f7f-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f7f-159">-WhatIf</span></span>
<span data-ttu-id="99f7f-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99f7f-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f7f-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99f7f-161">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="99f7f-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99f7f-162">INPUTS</span></span>

### <span data-ttu-id="99f7f-163">Microsoft. WindowsAzure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="99f7f-164">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer System. String Microsoft. WindowsAzure. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="99f7f-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="99f7f-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99f7f-165">OUTPUTS</span></span>

### <span data-ttu-id="99f7f-166">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="99f7f-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="99f7f-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99f7f-167">NOTES</span></span>

## <span data-ttu-id="99f7f-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99f7f-168">RELATED LINKS</span></span>

