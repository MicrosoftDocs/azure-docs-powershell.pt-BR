---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 104a5b1ff5cde0f3ea55a29e87e38e6adaaf0488
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776276"
---
# <span data-ttu-id="1476a-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1476a-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="1476a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1476a-102">SYNOPSIS</span></span>
<span data-ttu-id="1476a-103">Lista os BLOBs em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="1476a-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="1476a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1476a-104">SYNTAX</span></span>

### <span data-ttu-id="1476a-105">Blobname (padrão)</span><span class="sxs-lookup"><span data-stu-id="1476a-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1476a-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="1476a-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="1476a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1476a-107">DESCRIPTION</span></span>
<span data-ttu-id="1476a-108">O cmdlet **Get-AzStorageBlob** lista BLOBs no contêiner especificado em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1476a-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="1476a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1476a-109">EXAMPLES</span></span>

### <span data-ttu-id="1476a-110">Exemplo 1: obter um blob por nome de BLOB</span><span class="sxs-lookup"><span data-stu-id="1476a-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="1476a-111">Esse comando usa um nome de BLOB e um curinga para obter um blob.</span><span class="sxs-lookup"><span data-stu-id="1476a-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="1476a-112">Exemplo 2: obter BLOBs em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="1476a-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="1476a-113">Esse comando usa o pipeline para obter todos os BLOBs (incluir BLOBs no status excluído) em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="1476a-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="1476a-114">Exemplo 3: obter blobs por prefixo de nome</span><span class="sxs-lookup"><span data-stu-id="1476a-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="1476a-115">Esse comando usa um prefixo Name para obter BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1476a-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="1476a-116">Exemplo 4: listar BLOBs em vários lotes</span><span class="sxs-lookup"><span data-stu-id="1476a-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="1476a-117">Este exemplo usa os parâmetros *MaxCount* e *ContinuationToken* para listar blobs de armazenamento do Azure em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="1476a-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="1476a-118">Os quatro primeiros comandos atribuem valores a variáveis a serem usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="1476a-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="1476a-119">O quinto comando especifica uma instrução **do while** que usa o cmdlet **Get-AzStorageBlob** para obter BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1476a-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="1476a-120">A instrução inclui o token de continuação armazenado na variável $Token.</span><span class="sxs-lookup"><span data-stu-id="1476a-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="1476a-121">$Token altera o valor conforme o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="1476a-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="1476a-122">Para obter mais informações, digite `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="1476a-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="1476a-123">O comando final usa o comando **Echo** para exibir o total.</span><span class="sxs-lookup"><span data-stu-id="1476a-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="1476a-124">OS</span><span class="sxs-lookup"><span data-stu-id="1476a-124">PARAMETERS</span></span>

### <span data-ttu-id="1476a-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="1476a-125">-Blob</span></span>
<span data-ttu-id="1476a-126">Especifica um padrão de nome ou nome, que pode ser usado para uma pesquisa por curinga.</span><span class="sxs-lookup"><span data-stu-id="1476a-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="1476a-127">Se não for especificado um nome de BLOB, o cmdlet listará todos os BLOBs no contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="1476a-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="1476a-128">Se um valor for especificado para esse parâmetro, o cmdlet listará todos os BLOBs com nomes correspondentes a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1476a-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1476a-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1476a-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1476a-130">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1476a-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1476a-131">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1476a-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1476a-132">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1476a-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1476a-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1476a-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1476a-134">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1476a-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1476a-135">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1476a-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1476a-136">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1476a-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1476a-137">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1476a-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1476a-138">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1476a-138">The default value is 10.</span></span>

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

### <span data-ttu-id="1476a-139">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1476a-139">-Container</span></span>
<span data-ttu-id="1476a-140">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1476a-140">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1476a-141">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1476a-141">-Context</span></span>
<span data-ttu-id="1476a-142">Especifica a conta de armazenamento do Azure da qual você deseja obter uma lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1476a-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="1476a-143">Você pode usar o cmdlet New-AzStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1476a-143">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="1476a-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="1476a-144">-ContinuationToken</span></span>
<span data-ttu-id="1476a-145">Especifica um token de continuação para a lista de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1476a-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="1476a-146">Use esse parâmetro e o parâmetro *MaxCount* para listar BLOBs em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="1476a-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1476a-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1476a-147">-DefaultProfile</span></span>
<span data-ttu-id="1476a-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1476a-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1476a-149">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="1476a-149">-IncludeDeleted</span></span>
<span data-ttu-id="1476a-150">Incluir blob excluído, por padrão obter BLOB não inclui blob excluído.</span><span class="sxs-lookup"><span data-stu-id="1476a-150">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="1476a-151">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1476a-151">-MaxCount</span></span>
<span data-ttu-id="1476a-152">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="1476a-152">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="1476a-153">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1476a-153">-Prefix</span></span>
<span data-ttu-id="1476a-154">Especifica um prefixo para os nomes de BLOB que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="1476a-154">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="1476a-155">Esse parâmetro não oferece suporte ao uso de expressões regulares ou caracteres curinga para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1476a-155">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="1476a-156">Isso significa que, se o contêiner tiver apenas BLOBs denominados "My", "MyBlob1" e "MyBlob2" e você especificar "-prefix My \*", o cmdlet retornará nenhum blob.</span><span class="sxs-lookup"><span data-stu-id="1476a-156">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="1476a-157">No entanto, se você especificar "-prefix My", o cmdlet retornará "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="1476a-157">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1476a-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1476a-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1476a-159">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1476a-159">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1476a-160">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1476a-160">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1476a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1476a-161">CommonParameters</span></span>
<span data-ttu-id="1476a-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1476a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1476a-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1476a-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1476a-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1476a-164">INPUTS</span></span>

### <span data-ttu-id="1476a-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1476a-165">System.String</span></span>

### <span data-ttu-id="1476a-166">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1476a-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1476a-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1476a-167">OUTPUTS</span></span>

### <span data-ttu-id="1476a-168">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1476a-168">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1476a-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1476a-169">NOTES</span></span>

## <span data-ttu-id="1476a-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1476a-170">RELATED LINKS</span></span>

[<span data-ttu-id="1476a-171">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1476a-171">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="1476a-172">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1476a-172">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="1476a-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1476a-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


