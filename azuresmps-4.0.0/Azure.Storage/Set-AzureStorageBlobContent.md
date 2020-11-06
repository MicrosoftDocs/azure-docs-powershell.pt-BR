---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426097"
---
# <span data-ttu-id="82854-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82854-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="82854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82854-102">SYNOPSIS</span></span>
<span data-ttu-id="82854-103">Carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="82854-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="82854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82854-104">SYNTAX</span></span>

### <span data-ttu-id="82854-105">SendManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="82854-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82854-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="82854-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82854-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="82854-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82854-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82854-108">DESCRIPTION</span></span>
<span data-ttu-id="82854-109">O cmdlet **set-AzureStorageBlobContent** carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="82854-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="82854-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82854-110">EXAMPLES</span></span>

### <span data-ttu-id="82854-111">Exemplo 1: carregar um arquivo nomeado</span><span class="sxs-lookup"><span data-stu-id="82854-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="82854-112">Esse comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.</span><span class="sxs-lookup"><span data-stu-id="82854-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="82854-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="82854-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="82854-114">Esse comando usa o cmdlet principal do Windows PowerShell Get-ChildItem para obter todos os arquivos na pasta atual e em subpastas e, em seguida, passá-los para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="82854-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="82854-115">O cmdlet **set-AzureStorageBlobContent** carrega os arquivos para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="82854-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="82854-116">Exemplo 3: substituir um blob existente</span><span class="sxs-lookup"><span data-stu-id="82854-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="82854-117">Esse comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzureStorageBlob e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="82854-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="82854-118">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="82854-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="82854-119">Esse comando não especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="82854-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="82854-120">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="82854-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="82854-121">Se você confirmar o comando, o cmdlet substituirá o blob existente.</span><span class="sxs-lookup"><span data-stu-id="82854-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="82854-122">Exemplo 4: carregar um arquivo em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="82854-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="82854-123">Esse comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzureStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="82854-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="82854-124">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="82854-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="82854-125">Exemplo 5: carregar um arquivo e metadados</span><span class="sxs-lookup"><span data-stu-id="82854-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="82854-126">O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na variável $Metadata.</span><span class="sxs-lookup"><span data-stu-id="82854-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="82854-127">O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="82854-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="82854-128">O blob inclui os metadados armazenados em $Metadata.</span><span class="sxs-lookup"><span data-stu-id="82854-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="82854-129">OS</span><span class="sxs-lookup"><span data-stu-id="82854-129">PARAMETERS</span></span>

### <span data-ttu-id="82854-130">-Blob</span><span class="sxs-lookup"><span data-stu-id="82854-130">-Blob</span></span>
<span data-ttu-id="82854-131">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="82854-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="82854-132">Esse cmdlet carrega um arquivo para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="82854-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82854-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="82854-133">-BlobType</span></span>
<span data-ttu-id="82854-134">Especifica o tipo do blob que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="82854-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="82854-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="82854-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82854-136">Block</span><span class="sxs-lookup"><span data-stu-id="82854-136">Block</span></span>
- <span data-ttu-id="82854-137">Page</span><span class="sxs-lookup"><span data-stu-id="82854-137">Page</span></span>

<span data-ttu-id="82854-138">O valor padrão é bloquear.</span><span class="sxs-lookup"><span data-stu-id="82854-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82854-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="82854-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="82854-140">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="82854-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="82854-141">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="82854-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="82854-142">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="82854-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="82854-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="82854-143">-CloudBlob</span></span>
<span data-ttu-id="82854-144">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="82854-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="82854-145">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="82854-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="82854-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="82854-146">-CloudBlobContainer</span></span>
<span data-ttu-id="82854-147">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="82854-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="82854-148">Esse cmdlet carrega o conteúdo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="82854-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="82854-149">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="82854-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="82854-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="82854-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="82854-151">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="82854-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="82854-152">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="82854-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="82854-153">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="82854-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="82854-154">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="82854-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="82854-155">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="82854-155">The default value is 10.</span></span>

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

### <span data-ttu-id="82854-156">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="82854-156">-Container</span></span>
<span data-ttu-id="82854-157">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="82854-157">Specifies the name of a container.</span></span>
<span data-ttu-id="82854-158">Esse cmdlet carrega um arquivo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="82854-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82854-159">-Contexto</span><span class="sxs-lookup"><span data-stu-id="82854-159">-Context</span></span>
<span data-ttu-id="82854-160">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="82854-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="82854-161">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="82854-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="82854-162">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="82854-162">-File</span></span>
<span data-ttu-id="82854-163">Especifica um caminho de arquivo local para o carregamento de um arquivo como conteúdo BLOB.</span><span class="sxs-lookup"><span data-stu-id="82854-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82854-164">-Force</span><span class="sxs-lookup"><span data-stu-id="82854-164">-Force</span></span>
<span data-ttu-id="82854-165">Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="82854-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="82854-166">-Metadados</span><span class="sxs-lookup"><span data-stu-id="82854-166">-Metadata</span></span>
<span data-ttu-id="82854-167">Especifica metadados para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="82854-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82854-168">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="82854-168">-Properties</span></span>
<span data-ttu-id="82854-169">Especifica as propriedades do blob carregado.</span><span class="sxs-lookup"><span data-stu-id="82854-169">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82854-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="82854-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="82854-171">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="82854-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="82854-172">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="82854-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="82854-173">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82854-173">-Confirm</span></span>
<span data-ttu-id="82854-174">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82854-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82854-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82854-175">-WhatIf</span></span>
<span data-ttu-id="82854-176">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82854-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82854-177">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82854-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82854-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82854-178">CommonParameters</span></span>
<span data-ttu-id="82854-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82854-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82854-180">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82854-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82854-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82854-181">INPUTS</span></span>

## <span data-ttu-id="82854-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82854-182">OUTPUTS</span></span>

## <span data-ttu-id="82854-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82854-183">NOTES</span></span>

## <span data-ttu-id="82854-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82854-184">RELATED LINKS</span></span>

[<span data-ttu-id="82854-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="82854-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="82854-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82854-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="82854-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="82854-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
