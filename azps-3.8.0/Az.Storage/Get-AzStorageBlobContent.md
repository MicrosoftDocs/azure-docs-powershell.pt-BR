---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 3f8c85ac8f6a93438176fb20acd98fdb84733927
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941241"
---
# <span data-ttu-id="cf013-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cf013-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="cf013-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf013-102">SYNOPSIS</span></span>
<span data-ttu-id="cf013-103">Baixa um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cf013-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="cf013-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf013-104">SYNTAX</span></span>

### <span data-ttu-id="cf013-105">ReceiveManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf013-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf013-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="cf013-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf013-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="cf013-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf013-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf013-108">DESCRIPTION</span></span>
<span data-ttu-id="cf013-109">O cmdlet **Get-AzStorageBlobContent** baixa o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="cf013-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="cf013-110">Se o nome do BLOB não for válido para o computador local, esse cmdlet o resolverá automaticamente se possível.</span><span class="sxs-lookup"><span data-stu-id="cf013-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="cf013-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf013-111">EXAMPLES</span></span>

### <span data-ttu-id="cf013-112">Exemplo 1: baixar conteúdo do blob por nome</span><span class="sxs-lookup"><span data-stu-id="cf013-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="cf013-113">Esse comando baixa um blob por nome.</span><span class="sxs-lookup"><span data-stu-id="cf013-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="cf013-114">Exemplo 2: baixar o conteúdo do blob usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="cf013-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="cf013-115">Esse comando usa o pipeline para localizar e baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="cf013-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="cf013-116">Exemplo 3: baixar o conteúdo do blob usando o pipeline e um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="cf013-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="cf013-117">Este exemplo usa o caractere curinga asterisco e o pipeline para localizar e baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="cf013-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="cf013-118">Exemplo 4: obter um objeto BLOB e salvá-lo em uma variável e, em seguida, baixar o conteúdo do blob com o objeto BLOB</span><span class="sxs-lookup"><span data-stu-id="cf013-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="cf013-119">Primeiro, este exemplo obtém um objeto BLOB e o salva em uma variável e, em seguida, baixa o conteúdo do blob com o objeto BLOB.</span><span class="sxs-lookup"><span data-stu-id="cf013-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="cf013-120">OS</span><span class="sxs-lookup"><span data-stu-id="cf013-120">PARAMETERS</span></span>

### <span data-ttu-id="cf013-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf013-121">-AsJob</span></span>
<span data-ttu-id="cf013-122">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="cf013-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cf013-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="cf013-123">-Blob</span></span>
<span data-ttu-id="cf013-124">Especifica o nome do blob a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="cf013-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="cf013-125">-CheckMd5</span></span>
<span data-ttu-id="cf013-126">Especifica se a soma MD5 deve ser verificada pelo arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="cf013-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="cf013-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf013-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf013-128">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf013-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf013-129">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cf013-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf013-130">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cf013-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf013-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cf013-131">-CloudBlob</span></span>
<span data-ttu-id="cf013-132">Especifica um blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="cf013-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="cf013-133">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="cf013-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cf013-134">-CloudBlobContainer</span></span>
<span data-ttu-id="cf013-135">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf013-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="cf013-136">Você pode criá-lo ou usar o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="cf013-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf013-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf013-138">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cf013-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf013-139">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cf013-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf013-140">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="cf013-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf013-141">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cf013-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf013-142">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cf013-142">The default value is 10.</span></span>

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

### <span data-ttu-id="cf013-143">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="cf013-143">-Container</span></span>
<span data-ttu-id="cf013-144">Especifica o nome do contêiner que tem o blob que você deseja baixar.</span><span class="sxs-lookup"><span data-stu-id="cf013-144">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-145">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cf013-145">-Context</span></span>
<span data-ttu-id="cf013-146">Especifica a conta de armazenamento do Azure da qual você deseja baixar o conteúdo do blob.</span><span class="sxs-lookup"><span data-stu-id="cf013-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="cf013-147">Você pode usar o cmdlet New-AzStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cf013-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf013-148">-DefaultProfile</span></span>
<span data-ttu-id="cf013-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf013-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf013-150">-Destino</span><span class="sxs-lookup"><span data-stu-id="cf013-150">-Destination</span></span>
<span data-ttu-id="cf013-151">Especifica o local para armazenar o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="cf013-151">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf013-152">-Force</span><span class="sxs-lookup"><span data-stu-id="cf013-152">-Force</span></span>
<span data-ttu-id="cf013-153">Substitui um arquivo existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="cf013-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="cf013-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf013-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf013-155">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cf013-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cf013-156">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cf013-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cf013-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf013-157">-Confirm</span></span>
<span data-ttu-id="cf013-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf013-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf013-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf013-159">-WhatIf</span></span>
<span data-ttu-id="cf013-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf013-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf013-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf013-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf013-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf013-162">CommonParameters</span></span>
<span data-ttu-id="cf013-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf013-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf013-164">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf013-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf013-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf013-165">INPUTS</span></span>

### <span data-ttu-id="cf013-166">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cf013-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cf013-167">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cf013-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cf013-168">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cf013-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf013-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf013-169">OUTPUTS</span></span>

### <span data-ttu-id="cf013-170">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf013-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cf013-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf013-171">NOTES</span></span>
* <span data-ttu-id="cf013-172">Se o nome do blob for inválido para o computador local, esse cmdlet o resolverá, se possível.</span><span class="sxs-lookup"><span data-stu-id="cf013-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="cf013-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf013-173">RELATED LINKS</span></span>

[<span data-ttu-id="cf013-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cf013-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="cf013-175">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf013-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="cf013-176">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf013-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
