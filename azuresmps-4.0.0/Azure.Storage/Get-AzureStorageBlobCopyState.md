---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3191d7369597fbfb0781b550a57f0032f9aaad4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426165"
---
# <span data-ttu-id="29ab1-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="29ab1-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="29ab1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="29ab1-103">Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab1-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="29ab1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29ab1-104">SYNTAX</span></span>

### <span data-ttu-id="29ab1-105">NamePipeline (padrão)</span><span class="sxs-lookup"><span data-stu-id="29ab1-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="29ab1-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="29ab1-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="29ab1-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="29ab1-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="29ab1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="29ab1-109">O cmdlet **Get-AzureStorageBlobCopyState** Obtém o status da cópia de um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab1-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="29ab1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="29ab1-111">Exemplo 1: obter o status da cópia de um blob</span><span class="sxs-lookup"><span data-stu-id="29ab1-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="29ab1-112">Esse comando obtém o status da cópia do blob chamado ContosoPlanning2015 na ContosoUploads do contêiner.</span><span class="sxs-lookup"><span data-stu-id="29ab1-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="29ab1-113">Exemplo 2: obter o status da cópia de um BLOB usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="29ab1-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="29ab1-114">Esse comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads usando o cmdlet **Get-AzureStorageBlob** e, em seguida, passa o resultado para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="29ab1-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29ab1-115">O cmdlet **Get-AzureStorageBlobCopyState** Obtém o status de cópia desse blob.</span><span class="sxs-lookup"><span data-stu-id="29ab1-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="29ab1-116">Exemplo 3: obter o status da cópia de um blob em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="29ab1-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="29ab1-117">Esse comando obtém o contêiner nomeado usando o cmdlet **Get-AzureStorageBlob** e, em seguida, passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="29ab1-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="29ab1-118">O cmdlet **Get-AzureStorageContainer** Obtém o status de cópia do blob chamado ContosoPlanning2015 nesse contêiner.</span><span class="sxs-lookup"><span data-stu-id="29ab1-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="29ab1-119">OS</span><span class="sxs-lookup"><span data-stu-id="29ab1-119">PARAMETERS</span></span>

### <span data-ttu-id="29ab1-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="29ab1-120">-Blob</span></span>
<span data-ttu-id="29ab1-121">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="29ab1-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="29ab1-122">Esse cmdlet obtém o estado da operação de cópia de BLOB para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="29ab1-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="29ab1-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29ab1-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="29ab1-124">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="29ab1-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="29ab1-125">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="29ab1-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="29ab1-126">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="29ab1-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="29ab1-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="29ab1-127">-CloudBlob</span></span>
<span data-ttu-id="29ab1-128">Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab1-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="29ab1-129">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="29ab1-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="29ab1-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="29ab1-130">-CloudBlobContainer</span></span>
<span data-ttu-id="29ab1-131">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab1-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="29ab1-132">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="29ab1-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="29ab1-133">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="29ab1-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="29ab1-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29ab1-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29ab1-135">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="29ab1-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="29ab1-136">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="29ab1-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="29ab1-137">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="29ab1-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="29ab1-138">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="29ab1-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="29ab1-139">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="29ab1-139">The default value is 10.</span></span>

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

### <span data-ttu-id="29ab1-140">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="29ab1-140">-Container</span></span>
<span data-ttu-id="29ab1-141">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="29ab1-141">Specifies the name of a container.</span></span>
<span data-ttu-id="29ab1-142">Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="29ab1-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="29ab1-143">-Contexto</span><span class="sxs-lookup"><span data-stu-id="29ab1-143">-Context</span></span>
<span data-ttu-id="29ab1-144">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab1-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="29ab1-145">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="29ab1-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="29ab1-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29ab1-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="29ab1-147">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="29ab1-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="29ab1-148">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="29ab1-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="29ab1-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="29ab1-149">-WaitForComplete</span></span>
<span data-ttu-id="29ab1-150">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="29ab1-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="29ab1-151">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="29ab1-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="29ab1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ab1-152">CommonParameters</span></span>
<span data-ttu-id="29ab1-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ab1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ab1-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ab1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ab1-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29ab1-155">INPUTS</span></span>

## <span data-ttu-id="29ab1-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29ab1-156">OUTPUTS</span></span>

### <span data-ttu-id="29ab1-157">CopyState</span><span class="sxs-lookup"><span data-stu-id="29ab1-157">CopyState</span></span>

## <span data-ttu-id="29ab1-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29ab1-158">NOTES</span></span>

## <span data-ttu-id="29ab1-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29ab1-159">RELATED LINKS</span></span>

[<span data-ttu-id="29ab1-160">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="29ab1-160">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="29ab1-161">Parar-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="29ab1-161">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)

