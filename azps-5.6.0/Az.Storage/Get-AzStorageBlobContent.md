---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: b3c2e5809cf2f9aa13a11600351c64a825caf5d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891996"
---
# <span data-ttu-id="de1da-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="de1da-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="de1da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de1da-102">SYNOPSIS</span></span>
<span data-ttu-id="de1da-103">Baixa um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="de1da-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="de1da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de1da-104">SYNTAX</span></span>

### <span data-ttu-id="de1da-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de1da-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de1da-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="de1da-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de1da-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="de1da-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de1da-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de1da-108">DESCRIPTION</span></span>
<span data-ttu-id="de1da-109">O cmdlet **Get-AzStorageBlobContent** baixa o blob de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="de1da-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="de1da-110">Se o nome blob não for válido para o computador local, esse cmdlet o resolverá automaticamente se for possível.</span><span class="sxs-lookup"><span data-stu-id="de1da-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="de1da-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de1da-111">EXAMPLES</span></span>

### <span data-ttu-id="de1da-112">Exemplo 1: Baixar conteúdo de blob pelo nome</span><span class="sxs-lookup"><span data-stu-id="de1da-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="de1da-113">Este comando baixa um blob pelo nome.</span><span class="sxs-lookup"><span data-stu-id="de1da-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="de1da-114">Exemplo 2: Baixar conteúdo de blob usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="de1da-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="de1da-115">Este comando usa o pipeline para encontrar e baixar conteúdo blob.</span><span class="sxs-lookup"><span data-stu-id="de1da-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="de1da-116">Exemplo 3: Baixar conteúdo blob usando o pipeline e um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="de1da-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="de1da-117">Este exemplo usa o caractere curinga asterisco e o pipeline para encontrar e baixar conteúdo de blob.</span><span class="sxs-lookup"><span data-stu-id="de1da-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="de1da-118">Exemplo 4: obter um objeto blob e salvá-lo em uma variável e baixar conteúdo blob com o objeto blob</span><span class="sxs-lookup"><span data-stu-id="de1da-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="de1da-119">Este exemplo primeiro obter um objeto blob e salvá-lo em uma variável, em seguida, baixar conteúdo blob com o objeto blob.</span><span class="sxs-lookup"><span data-stu-id="de1da-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="de1da-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de1da-120">PARAMETERS</span></span>

### <span data-ttu-id="de1da-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de1da-121">-AsJob</span></span>
<span data-ttu-id="de1da-122">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="de1da-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="de1da-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="de1da-123">-Blob</span></span>
<span data-ttu-id="de1da-124">Especifica o nome do blob a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="de1da-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="de1da-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="de1da-125">-BlobBaseClient</span></span>
<span data-ttu-id="de1da-126">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="de1da-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de1da-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="de1da-127">-CheckMd5</span></span>
<span data-ttu-id="de1da-128">Especifica se a soma Md5 deve ser consultada para o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="de1da-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="de1da-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de1da-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="de1da-130">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="de1da-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de1da-131">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="de1da-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de1da-132">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="de1da-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="de1da-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="de1da-133">-CloudBlob</span></span>
<span data-ttu-id="de1da-134">Especifica um blob de nuvem.</span><span class="sxs-lookup"><span data-stu-id="de1da-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="de1da-135">Para obter um **objeto CloudBlob,** use Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de1da-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="de1da-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="de1da-136">-CloudBlobContainer</span></span>
<span data-ttu-id="de1da-137">Especifica um **objeto CloudBlobContainer** da biblioteca de clientes de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="de1da-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="de1da-138">Você pode criar ou usar o cmdlet Get-AzStorageContainer usuário.</span><span class="sxs-lookup"><span data-stu-id="de1da-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="de1da-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="de1da-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="de1da-140">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="de1da-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="de1da-141">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="de1da-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="de1da-142">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="de1da-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="de1da-143">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="de1da-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="de1da-144">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="de1da-144">The default value is 10.</span></span>

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

### <span data-ttu-id="de1da-145">-Container</span><span class="sxs-lookup"><span data-stu-id="de1da-145">-Container</span></span>
<span data-ttu-id="de1da-146">Especifica o nome do contêiner que tem o blob que você deseja baixar.</span><span class="sxs-lookup"><span data-stu-id="de1da-146">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="de1da-147">-Context</span><span class="sxs-lookup"><span data-stu-id="de1da-147">-Context</span></span>
<span data-ttu-id="de1da-148">Especifica a conta de armazenamento do Azure da qual você deseja baixar conteúdo de blob.</span><span class="sxs-lookup"><span data-stu-id="de1da-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="de1da-149">Você pode usar o cmdlet New-AzStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="de1da-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="de1da-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1da-150">-DefaultProfile</span></span>
<span data-ttu-id="de1da-151">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de1da-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de1da-152">-Destination</span><span class="sxs-lookup"><span data-stu-id="de1da-152">-Destination</span></span>
<span data-ttu-id="de1da-153">Especifica o local para armazenar o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="de1da-153">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="de1da-154">-Force</span><span class="sxs-lookup"><span data-stu-id="de1da-154">-Force</span></span>
<span data-ttu-id="de1da-155">Substitui um arquivo existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="de1da-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="de1da-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de1da-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="de1da-157">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="de1da-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="de1da-158">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="de1da-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="de1da-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de1da-159">-Confirm</span></span>
<span data-ttu-id="de1da-160">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de1da-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de1da-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de1da-161">-WhatIf</span></span>
<span data-ttu-id="de1da-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de1da-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de1da-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de1da-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de1da-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1da-164">CommonParameters</span></span>
<span data-ttu-id="de1da-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1da-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1da-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1da-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1da-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de1da-167">INPUTS</span></span>

### <span data-ttu-id="de1da-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="de1da-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="de1da-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="de1da-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="de1da-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="de1da-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="de1da-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de1da-171">OUTPUTS</span></span>

### <span data-ttu-id="de1da-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de1da-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="de1da-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="de1da-173">NOTES</span></span>
* <span data-ttu-id="de1da-174">Se o nome do blob for inválido para o computador local, este cmdlet o autoritará, se possível.</span><span class="sxs-lookup"><span data-stu-id="de1da-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="de1da-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de1da-175">RELATED LINKS</span></span>

[<span data-ttu-id="de1da-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="de1da-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="de1da-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de1da-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="de1da-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de1da-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
