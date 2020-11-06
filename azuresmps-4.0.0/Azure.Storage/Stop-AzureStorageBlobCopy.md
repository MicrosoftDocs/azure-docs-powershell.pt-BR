---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426198"
---
# <span data-ttu-id="9c7b7-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9c7b7-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="9c7b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7b7-103">Interrompe uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-103">Stops a copy operation.</span></span>

## <span data-ttu-id="9c7b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c7b7-104">SYNTAX</span></span>

### <span data-ttu-id="9c7b7-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c7b7-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7b7-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9c7b7-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7b7-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9c7b7-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c7b7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="9c7b7-109">O cmdlet **Stop-AzureStorageBlobCopy** interrompe uma operação de cópia para o blob de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="9c7b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c7b7-110">EXAMPLES</span></span>

### <span data-ttu-id="9c7b7-111">Exemplo 1: interromper a operação de cópia por nome</span><span class="sxs-lookup"><span data-stu-id="9c7b7-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="9c7b7-112">Esse comando interrompe a operação de cópia por nome.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="9c7b7-113">Exemplo 2: interromper a operação de cópia usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="9c7b7-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="9c7b7-114">Esse comando interrompe a operação de cópia passando o contêiner no pipeline de **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="9c7b7-115">Exemplo 3: interromper a operação de cópia usando o pipeline e Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c7b7-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="9c7b7-116">Este exemplo interrompe a operação de cópia passando o contêiner no pipeline do cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="9c7b7-117">OS</span><span class="sxs-lookup"><span data-stu-id="9c7b7-117">PARAMETERS</span></span>

### <span data-ttu-id="9c7b7-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="9c7b7-118">-Blob</span></span>
<span data-ttu-id="9c7b7-119">Especifica o nome do blob.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c7b7-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9c7b7-121">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9c7b7-122">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9c7b7-123">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9c7b7-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9c7b7-124">-CloudBlob</span></span>
<span data-ttu-id="9c7b7-125">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="9c7b7-126">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9c7b7-127">-CloudBlobContainer</span></span>
<span data-ttu-id="9c7b7-128">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9c7b7-129">Você pode criar o objeto ou usar o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9c7b7-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9c7b7-131">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9c7b7-132">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9c7b7-133">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9c7b7-134">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9c7b7-135">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-135">The default value is 10.</span></span>

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

### <span data-ttu-id="9c7b7-136">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="9c7b7-136">-Container</span></span>
<span data-ttu-id="9c7b7-137">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9c7b7-138">-Context</span></span>
<span data-ttu-id="9c7b7-139">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9c7b7-140">Você pode criar o contexto usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-141">-Copyid</span><span class="sxs-lookup"><span data-stu-id="9c7b7-141">-CopyId</span></span>
<span data-ttu-id="9c7b7-142">Especifica a ID da cópia.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c7b7-143">-Force</span><span class="sxs-lookup"><span data-stu-id="9c7b7-143">-Force</span></span>
<span data-ttu-id="9c7b7-144">Interrompe a tarefa atual de copiar no blob especificado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9c7b7-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c7b7-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9c7b7-146">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9c7b7-147">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9c7b7-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c7b7-148">-Confirm</span></span>
<span data-ttu-id="9c7b7-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7b7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7b7-150">-WhatIf</span></span>
<span data-ttu-id="9c7b7-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7b7-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7b7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7b7-153">CommonParameters</span></span>
<span data-ttu-id="9c7b7-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c7b7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7b7-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7b7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7b7-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c7b7-156">INPUTS</span></span>

## <span data-ttu-id="9c7b7-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c7b7-157">OUTPUTS</span></span>

## <span data-ttu-id="9c7b7-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c7b7-158">NOTES</span></span>

## <span data-ttu-id="9c7b7-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c7b7-159">RELATED LINKS</span></span>

[<span data-ttu-id="9c7b7-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c7b7-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9c7b7-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c7b7-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="9c7b7-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9c7b7-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="9c7b7-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="9c7b7-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)