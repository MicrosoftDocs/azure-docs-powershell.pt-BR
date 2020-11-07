---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 28d0c33a1aa74b5c5f69670622cc12c48810906f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776140"
---
# <span data-ttu-id="52b79-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="52b79-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="52b79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52b79-102">SYNOPSIS</span></span>
<span data-ttu-id="52b79-103">Iniciar uma operação de cópia incremental de um instantâneo de blob de página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="52b79-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="52b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52b79-104">SYNTAX</span></span>

### <span data-ttu-id="52b79-105">ContainerInstance (padrão)</span><span class="sxs-lookup"><span data-stu-id="52b79-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b79-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="52b79-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b79-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="52b79-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b79-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="52b79-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b79-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="52b79-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b79-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52b79-110">DESCRIPTION</span></span>
<span data-ttu-id="52b79-111">Iniciar uma operação de cópia incremental de um instantâneo de blob de página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="52b79-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="52b79-112">Veja mais detalhes do recurso em https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="52b79-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="52b79-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52b79-113">EXAMPLES</span></span>

### <span data-ttu-id="52b79-114">Exemplo 1: iniciar a operação de cópia incremental por nome do blob e tempo do instantâneo</span><span class="sxs-lookup"><span data-stu-id="52b79-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="52b79-115">Este comando inicia a operação de cópia incremental por nome do blob e tempo do instantâneo</span><span class="sxs-lookup"><span data-stu-id="52b79-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="52b79-116">Exemplo 2: iniciar a operação de cópia incremental usando o URI de origem</span><span class="sxs-lookup"><span data-stu-id="52b79-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="52b79-117">Este comando inicia a operação de cópia incremental usando o URI de origem</span><span class="sxs-lookup"><span data-stu-id="52b79-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="52b79-118">Exemplo 3: iniciar a operação de cópia incremental usando o pipeline de contêiner de GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="52b79-119">Este comando inicia a operação de cópia incremental usando o pipeline de contêiner do GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="52b79-120">Exemplo 4: iniciar a operação de cópia incremental do objeto CloudPageBlob para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="52b79-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="52b79-121">Este comando inicia a operação de cópia incremental do objeto CloudPageBlob para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="52b79-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="52b79-122">OS</span><span class="sxs-lookup"><span data-stu-id="52b79-122">PARAMETERS</span></span>

### <span data-ttu-id="52b79-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="52b79-123">-AbsoluteUri</span></span>
<span data-ttu-id="52b79-124">URI absoluto para a fonte.</span><span class="sxs-lookup"><span data-stu-id="52b79-124">Absolute Uri to the source.</span></span> <span data-ttu-id="52b79-125">Lembre-se de que a credencial deve ser fornecida no URI, se a origem exigir algum.</span><span class="sxs-lookup"><span data-stu-id="52b79-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="52b79-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52b79-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="52b79-127">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="52b79-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="52b79-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-128">-CloudBlob</span></span>
<span data-ttu-id="52b79-129">Objeto CloudBlob da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="52b79-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="52b79-130">Você pode criá-lo ou usar Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b79-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-131">-CloudBlobContainer</span></span>
<span data-ttu-id="52b79-132">Objeto CloudBlobContainer da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="52b79-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="52b79-133">Você pode criá-lo ou usar Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b79-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="52b79-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="52b79-135">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="52b79-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="52b79-136">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="52b79-136">The default value is 10.</span></span>

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

### <span data-ttu-id="52b79-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="52b79-137">-Context</span></span>
<span data-ttu-id="52b79-138">Contexto de armazenamento do Azure de origem.</span><span class="sxs-lookup"><span data-stu-id="52b79-138">Source Azure Storage Context.</span></span> <span data-ttu-id="52b79-139">Você pode criá-lo por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b79-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="52b79-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b79-140">-DefaultProfile</span></span>
<span data-ttu-id="52b79-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52b79-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-142">-DestBlob</span></span>
<span data-ttu-id="52b79-143">Nome do blob de destino</span><span class="sxs-lookup"><span data-stu-id="52b79-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="52b79-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-144">-DestCloudBlob</span></span>
<span data-ttu-id="52b79-145">Objeto CloudBlob de destino</span><span class="sxs-lookup"><span data-stu-id="52b79-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-146">-DestContainer</span></span>
<span data-ttu-id="52b79-147">Nome do contêiner de destino</span><span class="sxs-lookup"><span data-stu-id="52b79-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="52b79-148">-DestContext</span></span>
<span data-ttu-id="52b79-149">Contexto de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="52b79-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="52b79-150">Você pode criá-lo por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b79-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="52b79-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52b79-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="52b79-152">O tempo limite do servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="52b79-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="52b79-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-153">-SrcBlob</span></span>
<span data-ttu-id="52b79-154">Nome do blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="52b79-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="52b79-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="52b79-156">Tempo de instantâneo do blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="52b79-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b79-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-157">-SrcContainer</span></span>
<span data-ttu-id="52b79-158">Nome do contêiner de origem</span><span class="sxs-lookup"><span data-stu-id="52b79-158">Source Container name</span></span>

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

### <span data-ttu-id="52b79-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52b79-159">-Confirm</span></span>
<span data-ttu-id="52b79-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b79-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b79-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b79-161">-WhatIf</span></span>
<span data-ttu-id="52b79-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52b79-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b79-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52b79-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b79-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b79-164">CommonParameters</span></span>
<span data-ttu-id="52b79-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b79-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b79-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b79-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b79-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52b79-167">INPUTS</span></span>

### <span data-ttu-id="52b79-168">Microsoft. WindowsAz. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-168">Microsoft.WindowsAz.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="52b79-169">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="52b79-169">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="52b79-170">System. String</span><span class="sxs-lookup"><span data-stu-id="52b79-170">System.String</span></span>

### <span data-ttu-id="52b79-171">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="52b79-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="52b79-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52b79-172">OUTPUTS</span></span>

### <span data-ttu-id="52b79-173">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="52b79-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="52b79-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52b79-174">NOTES</span></span>

## <span data-ttu-id="52b79-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52b79-175">RELATED LINKS</span></span>
