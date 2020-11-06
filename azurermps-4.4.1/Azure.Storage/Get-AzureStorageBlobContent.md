---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 9eb7337ee39ed0e9c4d179a6a89401398a0d80f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432706"
---
# <span data-ttu-id="ad262-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad262-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="ad262-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad262-102">SYNOPSIS</span></span>
<span data-ttu-id="ad262-103">Baixa um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad262-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad262-104">SYNTAX</span></span>

### <span data-ttu-id="ad262-105">ReceiveManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="ad262-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad262-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ad262-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad262-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ad262-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad262-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad262-108">DESCRIPTION</span></span>
<span data-ttu-id="ad262-109">O cmdlet **Get-AzureStorageBlobContent** baixa o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="ad262-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="ad262-110">Se o nome do BLOB não for válido para o computador local, esse cmdlet o resolverá automaticamente se possível.</span><span class="sxs-lookup"><span data-stu-id="ad262-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="ad262-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad262-111">EXAMPLES</span></span>

### <span data-ttu-id="ad262-112">Exemplo 1: baixar conteúdo do blob por nome</span><span class="sxs-lookup"><span data-stu-id="ad262-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="ad262-113">Esse comando baixa um blob por nome.</span><span class="sxs-lookup"><span data-stu-id="ad262-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="ad262-114">Exemplo 2: baixar o conteúdo do blob usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="ad262-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="ad262-115">Esse comando usa o pipeline para localizar e baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="ad262-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ad262-116">Exemplo 3: baixar o conteúdo do blob usando o pipeline e um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="ad262-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="ad262-117">Este exemplo usa o caractere curinga asterisco e o pipeline para localizar e baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="ad262-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="ad262-118">OS</span><span class="sxs-lookup"><span data-stu-id="ad262-118">PARAMETERS</span></span>

### <span data-ttu-id="ad262-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="ad262-119">-Blob</span></span>
<span data-ttu-id="ad262-120">Especifica o nome do blob a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="ad262-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad262-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ad262-121">-CheckMd5</span></span>
<span data-ttu-id="ad262-122">Especifica se a soma MD5 deve ser verificada pelo arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="ad262-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ad262-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad262-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ad262-124">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad262-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ad262-125">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ad262-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ad262-126">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ad262-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ad262-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ad262-127">-CloudBlob</span></span>
<span data-ttu-id="ad262-128">Especifica um blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="ad262-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="ad262-129">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ad262-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ad262-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ad262-130">-CloudBlobContainer</span></span>
<span data-ttu-id="ad262-131">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad262-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="ad262-132">Você pode criá-lo ou usar o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ad262-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="ad262-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ad262-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ad262-134">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ad262-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ad262-135">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ad262-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ad262-136">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="ad262-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ad262-137">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ad262-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ad262-138">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="ad262-138">The default value is 10.</span></span>

<span data-ttu-id="ad262-139">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="ad262-139">The default value is 10.</span></span>

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

### <span data-ttu-id="ad262-140">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="ad262-140">-Container</span></span>
<span data-ttu-id="ad262-141">Especifica o nome do contêiner que tem o blob que você deseja baixar.</span><span class="sxs-lookup"><span data-stu-id="ad262-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad262-142">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ad262-142">-Context</span></span>
<span data-ttu-id="ad262-143">Especifica a conta de armazenamento do Azure da qual você deseja baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="ad262-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="ad262-144">Você pode usar o cmdlet New-AzureStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad262-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="ad262-145">-Destino</span><span class="sxs-lookup"><span data-stu-id="ad262-145">-Destination</span></span>
<span data-ttu-id="ad262-146">Especifica o local para armazenar o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="ad262-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad262-147">-Force</span><span class="sxs-lookup"><span data-stu-id="ad262-147">-Force</span></span>
<span data-ttu-id="ad262-148">Substitui um arquivo existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="ad262-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="ad262-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad262-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ad262-150">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="ad262-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ad262-151">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ad262-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ad262-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad262-152">-Confirm</span></span>
<span data-ttu-id="ad262-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad262-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad262-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad262-154">-WhatIf</span></span>
<span data-ttu-id="ad262-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad262-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad262-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad262-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad262-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad262-157">CommonParameters</span></span>
<span data-ttu-id="ad262-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad262-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad262-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad262-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad262-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad262-160">INPUTS</span></span>

### <span data-ttu-id="ad262-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad262-161">IStorageContext</span></span>

<span data-ttu-id="ad262-162">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ad262-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ad262-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad262-163">OUTPUTS</span></span>

### <span data-ttu-id="ad262-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad262-164">AzureStorageContainer</span></span>

## <span data-ttu-id="ad262-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad262-165">NOTES</span></span>
* <span data-ttu-id="ad262-166">Se o nome do blob for inválido para o computador local, esse cmdlet o resolverá, se possível.</span><span class="sxs-lookup"><span data-stu-id="ad262-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="ad262-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad262-167">RELATED LINKS</span></span>

[<span data-ttu-id="ad262-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad262-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="ad262-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ad262-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ad262-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ad262-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)