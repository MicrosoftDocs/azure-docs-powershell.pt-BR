---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
gitcommit: https://github.com/Azure/azure-powershell/blob/f8503a90f782f51c8baa0360f98adb33f2a6f26f
ms.openlocfilehash: e05dc3ed962e7d1d4610663dd129c0977b784280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431261"
---
# <span data-ttu-id="4cf99-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4cf99-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="4cf99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cf99-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf99-103">Lista os BLOBs em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="4cf99-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cf99-104">SYNTAX</span></span>

### <span data-ttu-id="4cf99-105">Blobname (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cf99-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4cf99-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="4cf99-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4cf99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cf99-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf99-108">O cmdlet **Get-AzureStorageBlob** lista BLOBs no contêiner especificado em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf99-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="4cf99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cf99-109">EXAMPLES</span></span>

### <span data-ttu-id="4cf99-110">Exemplo 1: obter um blob por nome de BLOB</span><span class="sxs-lookup"><span data-stu-id="4cf99-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="4cf99-111">Esse comando usa um nome de BLOB e um curinga para obter um blob.</span><span class="sxs-lookup"><span data-stu-id="4cf99-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="4cf99-112">Exemplo 2: obter um BLOB usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="4cf99-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="4cf99-113">Esse comando usa o pipeline para obter um blob.</span><span class="sxs-lookup"><span data-stu-id="4cf99-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="4cf99-114">Exemplo 3: obter um blob por prefixo de nome</span><span class="sxs-lookup"><span data-stu-id="4cf99-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="4cf99-115">Esse comando usa um prefixo Name para obter um blob.</span><span class="sxs-lookup"><span data-stu-id="4cf99-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="4cf99-116">Exemplo 4: listar BLOBs em vários lotes</span><span class="sxs-lookup"><span data-stu-id="4cf99-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="4cf99-117">Este exemplo usa os parâmetros *MaxCount* e *ContinuationToken* para listar blobs de armazenamento do Azure em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="4cf99-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="4cf99-118">Os quatro primeiros comandos atribuem valores a variáveis a serem usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf99-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="4cf99-119">O quinto comando especifica uma instrução **do while** que usa o cmdlet **Get-AzureStorageBlob** para obter BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4cf99-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="4cf99-120">A instrução inclui o token de continuação armazenado na variável $Token.</span><span class="sxs-lookup"><span data-stu-id="4cf99-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="4cf99-121">$Token altera o valor conforme o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="4cf99-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="4cf99-122">Para obter mais informações, digite `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="4cf99-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="4cf99-123">O comando final usa o comando **Echo** para exibir o total.</span><span class="sxs-lookup"><span data-stu-id="4cf99-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="4cf99-124">OS</span><span class="sxs-lookup"><span data-stu-id="4cf99-124">PARAMETERS</span></span>

### <span data-ttu-id="4cf99-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="4cf99-125">-Blob</span></span>
<span data-ttu-id="4cf99-126">Especifica um padrão de nome ou nome, que pode ser usado para uma pesquisa por curinga.</span><span class="sxs-lookup"><span data-stu-id="4cf99-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="4cf99-127">Se não for especificado um nome de BLOB, o cmdlet listará todos os BLOBs no contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="4cf99-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="4cf99-128">Se um valor for especificado para esse parâmetro, o cmdlet listará todos os BLOBs com nomes correspondentes a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4cf99-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4cf99-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cf99-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cf99-130">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="4cf99-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cf99-131">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cf99-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cf99-132">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4cf99-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cf99-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cf99-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cf99-134">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cf99-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cf99-135">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4cf99-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cf99-136">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="4cf99-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cf99-137">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4cf99-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cf99-138">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="4cf99-138">The default value is 10.</span></span>

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

### <span data-ttu-id="4cf99-139">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="4cf99-139">-Container</span></span>
<span data-ttu-id="4cf99-140">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4cf99-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf99-141">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4cf99-141">-Context</span></span>
<span data-ttu-id="4cf99-142">Especifica a conta de armazenamento do Azure da qual você deseja obter uma lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4cf99-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="4cf99-143">Você pode usar o cmdlet New-AzureStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4cf99-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="4cf99-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="4cf99-144">-ContinuationToken</span></span>
<span data-ttu-id="4cf99-145">Especifica um token de continuação para a lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="4cf99-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="4cf99-146">Use esse parâmetro e o parâmetro *MaxCount* para listar BLOBs em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="4cf99-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf99-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4cf99-147">-MaxCount</span></span>
<span data-ttu-id="4cf99-148">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="4cf99-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="4cf99-149">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4cf99-149">-Prefix</span></span>
<span data-ttu-id="4cf99-150">Especifica um prefixo para os nomes de BLOB que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="4cf99-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="4cf99-151">Esse parâmetro não oferece suporte ao uso de expressões regulares ou caracteres curinga para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4cf99-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="4cf99-152">Isso significa que, se o contêiner tiver apenas BLOBs denominados "My", "MyBlob1" e "MyBlob2" e você especificar "-prefix My \*", o cmdlet retornará nenhum blob.</span><span class="sxs-lookup"><span data-stu-id="4cf99-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="4cf99-153">No entanto, se você especificar "-prefix My", o cmdlet retornará "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="4cf99-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf99-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cf99-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cf99-155">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4cf99-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4cf99-156">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4cf99-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4cf99-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf99-157">CommonParameters</span></span>
<span data-ttu-id="4cf99-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf99-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf99-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf99-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf99-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cf99-160">INPUTS</span></span>

### <span data-ttu-id="4cf99-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cf99-161">IStorageContext</span></span>

<span data-ttu-id="4cf99-162">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4cf99-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="4cf99-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cf99-163">OUTPUTS</span></span>

### <span data-ttu-id="4cf99-164">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4cf99-164">AzureStorageBlob</span></span>

## <span data-ttu-id="4cf99-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cf99-165">NOTES</span></span>


## <span data-ttu-id="4cf99-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cf99-166">RELATED LINKS</span></span>

[<span data-ttu-id="4cf99-167">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4cf99-167">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="4cf99-168">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4cf99-168">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="4cf99-169">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4cf99-169">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


