---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118910"
---
# <span data-ttu-id="afa46-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="afa46-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="afa46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afa46-102">SYNOPSIS</span></span>
<span data-ttu-id="afa46-103">Inicie uma operação de cópia incremental de um instantâneo de blob de Página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="afa46-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="afa46-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afa46-104">SYNTAX</span></span>

### <span data-ttu-id="afa46-105">ContainerInstance (Padrão)</span><span class="sxs-lookup"><span data-stu-id="afa46-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa46-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="afa46-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa46-107">BlobInstanceToB ltdainstance</span><span class="sxs-lookup"><span data-stu-id="afa46-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa46-108">Containername</span><span class="sxs-lookup"><span data-stu-id="afa46-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa46-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="afa46-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa46-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="afa46-110">DESCRIPTION</span></span>
<span data-ttu-id="afa46-111">Inicie uma operação de cópia incremental de um instantâneo de blob de Página para o blob de página de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="afa46-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="afa46-112">Veja mais detalhes do recurso em https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="afa46-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="afa46-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="afa46-113">EXAMPLES</span></span>

### <span data-ttu-id="afa46-114">Exemplo 1: Iniciar a Operação de Cópia Incremental por nome de blob e tempo de instantâneo</span><span class="sxs-lookup"><span data-stu-id="afa46-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="afa46-115">Este comando inicia a Operação de Cópia Incremental por nome de blob e tempo de instantâneo</span><span class="sxs-lookup"><span data-stu-id="afa46-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="afa46-116">Exemplo 2: Iniciar a operação de cópia incremental usando uri de origem</span><span class="sxs-lookup"><span data-stu-id="afa46-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="afa46-117">Este comando inicia a Operação de Cópia Incremental usando uri de origem</span><span class="sxs-lookup"><span data-stu-id="afa46-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="afa46-118">Exemplo 3: Iniciar a operação de cópia incremental usando o pipeline de contêiner do GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="afa46-119">Este comando inicia a Operação de Cópia Incremental usando o pipeline de contêiner do GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="afa46-120">Exemplo 4: iniciar a operação de cópia incremental do objeto CloudPageB incremental para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="afa46-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="afa46-121">Este comando inicia a Operação de Cópia Incremental do objeto CloudPageB incremental para o blob de destino com o nome do blob</span><span class="sxs-lookup"><span data-stu-id="afa46-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="afa46-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afa46-122">PARAMETERS</span></span>

### <span data-ttu-id="afa46-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="afa46-123">-AbsoluteUri</span></span>
<span data-ttu-id="afa46-124">Uri absoluto à fonte.</span><span class="sxs-lookup"><span data-stu-id="afa46-124">Absolute Uri to the source.</span></span> <span data-ttu-id="afa46-125">A credencial deve ser fornecida no Uri, se a fonte exigir alguma.</span><span class="sxs-lookup"><span data-stu-id="afa46-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="afa46-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="afa46-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="afa46-127">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="afa46-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="afa46-128">-CloudBlab</span><span class="sxs-lookup"><span data-stu-id="afa46-128">-CloudBlob</span></span>
<span data-ttu-id="afa46-129">Objeto CloudB ltd da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa46-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="afa46-130">Você pode criar ou usar Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa46-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afa46-131">-CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-131">-CloudBlobContainer</span></span>
<span data-ttu-id="afa46-132">Objeto CloudBltContainer da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa46-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="afa46-133">Você pode criar ou usar Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa46-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="afa46-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="afa46-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="afa46-135">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="afa46-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="afa46-136">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="afa46-136">The default value is 10.</span></span>

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

### <span data-ttu-id="afa46-137">-Contexto</span><span class="sxs-lookup"><span data-stu-id="afa46-137">-Context</span></span>
<span data-ttu-id="afa46-138">Contexto de armazenamento de origem do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa46-138">Source Azure Storage Context.</span></span> <span data-ttu-id="afa46-139">Você pode criar por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa46-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="afa46-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa46-140">-DefaultProfile</span></span>
<span data-ttu-id="afa46-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afa46-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa46-142">-DestB meteor</span><span class="sxs-lookup"><span data-stu-id="afa46-142">-DestBlob</span></span>
<span data-ttu-id="afa46-143">Nome de blob de destino</span><span class="sxs-lookup"><span data-stu-id="afa46-143">Destination blob name</span></span>

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

### <span data-ttu-id="afa46-144">-DestCloudBcloudBcloud</span><span class="sxs-lookup"><span data-stu-id="afa46-144">-DestCloudBlob</span></span>
<span data-ttu-id="afa46-145">Objeto CloudB ltd</span><span class="sxs-lookup"><span data-stu-id="afa46-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa46-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-146">-DestContainer</span></span>
<span data-ttu-id="afa46-147">Nome do contêiner de destino</span><span class="sxs-lookup"><span data-stu-id="afa46-147">Destination container name</span></span>

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

### <span data-ttu-id="afa46-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="afa46-148">-DestContext</span></span>
<span data-ttu-id="afa46-149">Contexto de armazenamento do Azure de Destino.</span><span class="sxs-lookup"><span data-stu-id="afa46-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="afa46-150">Você pode criar por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa46-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="afa46-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="afa46-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="afa46-152">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="afa46-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="afa46-153">-SrcB cdc</span><span class="sxs-lookup"><span data-stu-id="afa46-153">-SrcBlob</span></span>
<span data-ttu-id="afa46-154">Nome do blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="afa46-154">Source page blob name.</span></span>

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

### <span data-ttu-id="afa46-155">-SrcBnapSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="afa46-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="afa46-156">Hora do instantâneo de blob da página de origem.</span><span class="sxs-lookup"><span data-stu-id="afa46-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="afa46-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-157">-SrcContainer</span></span>
<span data-ttu-id="afa46-158">Nome do Contêiner de Origem</span><span class="sxs-lookup"><span data-stu-id="afa46-158">Source Container name</span></span>

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

### <span data-ttu-id="afa46-159">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="afa46-159">-Confirm</span></span>
<span data-ttu-id="afa46-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa46-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa46-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa46-161">-WhatIf</span></span>
<span data-ttu-id="afa46-162">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="afa46-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa46-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afa46-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa46-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa46-164">CommonParameters</span></span>
<span data-ttu-id="afa46-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa46-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa46-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa46-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa46-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="afa46-167">INPUTS</span></span>

### <span data-ttu-id="afa46-168">Microsoft.Azure.Storage.Blob.CloudPageBpageBpage</span><span class="sxs-lookup"><span data-stu-id="afa46-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="afa46-169">Microsoft.Azure.Storage.Blob.CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="afa46-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="afa46-170">System.String</span><span class="sxs-lookup"><span data-stu-id="afa46-170">System.String</span></span>

### <span data-ttu-id="afa46-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="afa46-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="afa46-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="afa46-172">OUTPUTS</span></span>

### <span data-ttu-id="afa46-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlab</span><span class="sxs-lookup"><span data-stu-id="afa46-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="afa46-174">Notas</span><span class="sxs-lookup"><span data-stu-id="afa46-174">NOTES</span></span>

## <span data-ttu-id="afa46-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa46-175">RELATED LINKS</span></span>
