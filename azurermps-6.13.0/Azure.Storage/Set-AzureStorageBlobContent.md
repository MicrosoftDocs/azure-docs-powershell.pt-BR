---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: edc2a178ac8fa1c3a009830decb62d60ece2a367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428663"
---
# <span data-ttu-id="bf7c1-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf7c1-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="bf7c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7c1-103">Carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf7c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf7c1-104">SYNTAX</span></span>

### <span data-ttu-id="bf7c1-105">SendManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf7c1-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf7c1-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="bf7c1-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf7c1-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="bf7c1-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf7c1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf7c1-108">DESCRIPTION</span></span>
<span data-ttu-id="bf7c1-109">O cmdlet **set-AzureStorageBlobContent** carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="bf7c1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf7c1-110">EXAMPLES</span></span>

### <span data-ttu-id="bf7c1-111">Exemplo 1: carregar um arquivo nomeado</span><span class="sxs-lookup"><span data-stu-id="bf7c1-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="bf7c1-112">Esse comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="bf7c1-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="bf7c1-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="bf7c1-114">Esse comando usa o cmdlet principal do Windows PowerShell Get-ChildItem para obter todos os arquivos na pasta atual e em subpastas e, em seguida, passá-los para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf7c1-115">O cmdlet **set-AzureStorageBlobContent** carrega os arquivos para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="bf7c1-116">Exemplo 3: substituir um blob existente</span><span class="sxs-lookup"><span data-stu-id="bf7c1-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="bf7c1-117">Esse comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzureStorageBlob e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="bf7c1-118">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="bf7c1-119">Esse comando não especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="bf7c1-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="bf7c1-120">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="bf7c1-121">Se você confirmar o comando, o cmdlet substituirá o blob existente.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="bf7c1-122">Exemplo 4: carregar um arquivo em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="bf7c1-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="bf7c1-123">Esse comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzureStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="bf7c1-124">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="bf7c1-125">Exemplo 5: carregar um arquivo no BLOB da página com metadados e PremiumPageBlobTier como P10</span><span class="sxs-lookup"><span data-stu-id="bf7c1-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="bf7c1-126">O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na variável $Metadata.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="bf7c1-127">O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="bf7c1-128">O blob inclui os metadados armazenados no $Metadata e tem PremiumPageBlobTier como P10.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="bf7c1-129">Exemplo 6: carregar um arquivo para blob com propriedades de blob especificadas</span><span class="sxs-lookup"><span data-stu-id="bf7c1-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="bf7c1-130">Esse comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads com as propriedades de blob especificadas.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="bf7c1-131">OS</span><span class="sxs-lookup"><span data-stu-id="bf7c1-131">PARAMETERS</span></span>

### <span data-ttu-id="bf7c1-132">-Blob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-132">-Blob</span></span>
<span data-ttu-id="bf7c1-133">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="bf7c1-134">Esse cmdlet carrega um arquivo para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="bf7c1-135">-BlobType</span></span>
<span data-ttu-id="bf7c1-136">Especifica o tipo do blob que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="bf7c1-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf7c1-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf7c1-138">Block</span><span class="sxs-lookup"><span data-stu-id="bf7c1-138">Block</span></span>
- <span data-ttu-id="bf7c1-139">Página o valor padrão é bloquear.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-139">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf7c1-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf7c1-141">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf7c1-142">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf7c1-143">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bf7c1-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-144">-CloudBlob</span></span>
<span data-ttu-id="bf7c1-145">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="bf7c1-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="bf7c1-146">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-146">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bf7c1-147">-CloudBlobContainer</span></span>
<span data-ttu-id="bf7c1-148">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="bf7c1-149">Esse cmdlet carrega o conteúdo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="bf7c1-150">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-150">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf7c1-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf7c1-152">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf7c1-153">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf7c1-154">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf7c1-155">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf7c1-156">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-156">The default value is 10.</span></span>

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

### <span data-ttu-id="bf7c1-157">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="bf7c1-157">-Container</span></span>
<span data-ttu-id="bf7c1-158">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-158">Specifies the name of a container.</span></span>
<span data-ttu-id="bf7c1-159">Esse cmdlet carrega um arquivo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-160">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bf7c1-160">-Context</span></span>
<span data-ttu-id="bf7c1-161">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf7c1-162">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-162">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="bf7c1-163">Para usar um contexto de armazenamento criado a partir de um token SAS sem permissão de leitura, é necessário o parâmetro Add-Force para ignorar a verificação de BLOB.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-163">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="bf7c1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7c1-164">-DefaultProfile</span></span>
<span data-ttu-id="bf7c1-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf7c1-166">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="bf7c1-166">-File</span></span>
<span data-ttu-id="bf7c1-167">Especifica um caminho de arquivo local para o carregamento de um arquivo como conteúdo BLOB.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-167">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-168">-Force</span><span class="sxs-lookup"><span data-stu-id="bf7c1-168">-Force</span></span>
<span data-ttu-id="bf7c1-169">Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-169">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bf7c1-170">-Metadados</span><span class="sxs-lookup"><span data-stu-id="bf7c1-170">-Metadata</span></span>
<span data-ttu-id="bf7c1-171">Especifica metadados para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-171">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-172">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="bf7c1-172">-PremiumPageBlobTier</span></span>
<span data-ttu-id="bf7c1-173">Camada de blob de página</span><span class="sxs-lookup"><span data-stu-id="bf7c1-173">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-174">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf7c1-174">-Properties</span></span>
<span data-ttu-id="bf7c1-175">Especifica as propriedades do blob carregado.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-175">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="bf7c1-176">As propriedades com suporte são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-176">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7c1-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf7c1-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf7c1-178">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="bf7c1-179">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bf7c1-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf7c1-180">-Confirm</span></span>
<span data-ttu-id="bf7c1-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf7c1-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf7c1-182">-WhatIf</span></span>
<span data-ttu-id="bf7c1-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf7c1-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf7c1-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7c1-185">CommonParameters</span></span>
<span data-ttu-id="bf7c1-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf7c1-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7c1-187">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf7c1-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7c1-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf7c1-188">INPUTS</span></span>

### <span data-ttu-id="bf7c1-189">System. String</span><span class="sxs-lookup"><span data-stu-id="bf7c1-189">System.String</span></span>

### <span data-ttu-id="bf7c1-190">Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bf7c1-190">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="bf7c1-191">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-191">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bf7c1-192">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf7c1-192">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bf7c1-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf7c1-193">OUTPUTS</span></span>

### <span data-ttu-id="bf7c1-194">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-194">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="bf7c1-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf7c1-195">NOTES</span></span>

## <span data-ttu-id="bf7c1-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf7c1-196">RELATED LINKS</span></span>

[<span data-ttu-id="bf7c1-197">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf7c1-197">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="bf7c1-198">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-198">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="bf7c1-199">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bf7c1-199">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)