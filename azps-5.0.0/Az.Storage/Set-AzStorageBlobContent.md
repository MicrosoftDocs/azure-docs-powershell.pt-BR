---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: a71995015a8345b3ba181d92ba17e4dd258b169b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115774"
---
# <span data-ttu-id="2e9e1-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e9e1-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="2e9e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9e1-103">Carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="2e9e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e9e1-104">SYNTAX</span></span>

### <span data-ttu-id="2e9e1-105">SendManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9e1-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2e9e1-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e9e1-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2e9e1-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e9e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e9e1-108">DESCRIPTION</span></span>
<span data-ttu-id="2e9e1-109">O cmdlet **set-AzStorageBlobContent** carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="2e9e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e9e1-110">EXAMPLES</span></span>

### <span data-ttu-id="2e9e1-111">Exemplo 1: carregar um arquivo nomeado</span><span class="sxs-lookup"><span data-stu-id="2e9e1-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="2e9e1-112">Esse comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="2e9e1-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="2e9e1-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="2e9e1-114">Esse comando usa o cmdlet principal do Windows PowerShell Get-ChildItem para obter todos os arquivos na pasta atual e em subpastas e, em seguida, passá-los para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2e9e1-115">O cmdlet **set-AzStorageBlobContent** carrega os arquivos para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="2e9e1-116">Exemplo 3: substituir um blob existente</span><span class="sxs-lookup"><span data-stu-id="2e9e1-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="2e9e1-117">Esse comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzStorageBlob e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2e9e1-118">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="2e9e1-119">Esse comando não especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="2e9e1-120">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="2e9e1-121">Se você confirmar o comando, o cmdlet substituirá o blob existente.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="2e9e1-122">Exemplo 4: carregar um arquivo em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="2e9e1-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="2e9e1-123">Esse comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2e9e1-124">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="2e9e1-125">Exemplo 5: carregar um arquivo no BLOB da página com metadados e PremiumPageBlobTier como P10</span><span class="sxs-lookup"><span data-stu-id="2e9e1-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="2e9e1-126">O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na variável $Metadata.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="2e9e1-127">O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="2e9e1-128">O blob inclui os metadados armazenados no $Metadata e tem PremiumPageBlobTier como P10.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="2e9e1-129">Exemplo 6: carregar um arquivo para blob com propriedades de blob especificadas e definir StandardBlobTier como legal</span><span class="sxs-lookup"><span data-stu-id="2e9e1-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="2e9e1-130">Esse comando carrega o arquivo c:\temp\index.html para o contêiner chamado contosouploads com as propriedades de blob especificadas e define StandardBlobTier como legal.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="2e9e1-131">Esse comando obtém o valor ContentType definido como propriedades de blob por [System. Web. MimeMapping]:: GetMimeMapping () API.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="2e9e1-132">OS</span><span class="sxs-lookup"><span data-stu-id="2e9e1-132">PARAMETERS</span></span>

### <span data-ttu-id="2e9e1-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-133">-AsJob</span></span>
<span data-ttu-id="2e9e1-134">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2e9e1-135">-Blob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-135">-Blob</span></span>
<span data-ttu-id="2e9e1-136">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="2e9e1-137">Esse cmdlet carrega um arquivo para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e9e1-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="2e9e1-138">-BlobType</span></span>
<span data-ttu-id="2e9e1-139">Especifica o tipo do blob que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="2e9e1-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2e9e1-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e9e1-141">Block</span><span class="sxs-lookup"><span data-stu-id="2e9e1-141">Block</span></span>
- <span data-ttu-id="2e9e1-142">Página o valor padrão é bloquear.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-142">Page The default value is Block.</span></span>

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

### <span data-ttu-id="2e9e1-143">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e9e1-143">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2e9e1-144">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-144">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2e9e1-145">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-145">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2e9e1-146">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-146">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2e9e1-147">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-147">-CloudBlob</span></span>
<span data-ttu-id="2e9e1-148">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-148">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="2e9e1-149">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-149">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2e9e1-150">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2e9e1-150">-CloudBlobContainer</span></span>
<span data-ttu-id="2e9e1-151">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-151">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2e9e1-152">Esse cmdlet carrega o conteúdo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-152">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="2e9e1-153">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-153">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="2e9e1-154">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2e9e1-154">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2e9e1-155">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-155">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2e9e1-156">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-156">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2e9e1-157">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-157">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2e9e1-158">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-158">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2e9e1-159">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-159">The default value is 10.</span></span>

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

### <span data-ttu-id="2e9e1-160">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2e9e1-160">-Container</span></span>
<span data-ttu-id="2e9e1-161">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-161">Specifies the name of a container.</span></span>
<span data-ttu-id="2e9e1-162">Esse cmdlet carrega um arquivo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-162">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e9e1-163">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2e9e1-163">-Context</span></span>
<span data-ttu-id="2e9e1-164">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-164">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2e9e1-165">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-165">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="2e9e1-166">Para usar um contexto de armazenamento criado a partir de um token SAS sem permissão de leitura, é preciso ter o parâmetro Add-Force para ignorar a existência da verificação de BLOB.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-166">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="2e9e1-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9e1-167">-DefaultProfile</span></span>
<span data-ttu-id="2e9e1-168">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-168">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e9e1-169">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="2e9e1-169">-File</span></span>
<span data-ttu-id="2e9e1-170">Especifica um caminho de arquivo local para o carregamento de um arquivo como conteúdo BLOB.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-170">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="2e9e1-171">-Force</span><span class="sxs-lookup"><span data-stu-id="2e9e1-171">-Force</span></span>
<span data-ttu-id="2e9e1-172">Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-172">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2e9e1-173">-Metadados</span><span class="sxs-lookup"><span data-stu-id="2e9e1-173">-Metadata</span></span>
<span data-ttu-id="2e9e1-174">Especifica metadados para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-174">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="2e9e1-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="2e9e1-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="2e9e1-176">Camada de blob de página</span><span class="sxs-lookup"><span data-stu-id="2e9e1-176">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9e1-177">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e9e1-177">-Properties</span></span>
<span data-ttu-id="2e9e1-178">Especifica as propriedades do blob carregado.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-178">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="2e9e1-179">As propriedades com suporte são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-179">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="2e9e1-180">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e9e1-180">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2e9e1-181">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-181">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2e9e1-182">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-182">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2e9e1-183">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="2e9e1-183">-StandardBlobTier</span></span>
<span data-ttu-id="2e9e1-184">Camada de bloco de BLOB, os valores válidos são quente/interessante/arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-184">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="2e9e1-185">Veja detalhes em https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="2e9e1-185">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9e1-186">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e9e1-186">-Confirm</span></span>
<span data-ttu-id="2e9e1-187">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9e1-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9e1-188">-WhatIf</span></span>
<span data-ttu-id="2e9e1-189">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e9e1-190">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9e1-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9e1-191">CommonParameters</span></span>
<span data-ttu-id="2e9e1-192">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9e1-193">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9e1-194">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e9e1-194">INPUTS</span></span>

### <span data-ttu-id="2e9e1-195">System. String</span><span class="sxs-lookup"><span data-stu-id="2e9e1-195">System.String</span></span>

### <span data-ttu-id="2e9e1-196">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2e9e1-196">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2e9e1-197">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-197">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2e9e1-198">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e9e1-198">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2e9e1-199">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e9e1-199">OUTPUTS</span></span>

### <span data-ttu-id="2e9e1-200">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-200">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2e9e1-201">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e9e1-201">NOTES</span></span>

## <span data-ttu-id="2e9e1-202">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e9e1-202">RELATED LINKS</span></span>

[<span data-ttu-id="2e9e1-203">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2e9e1-203">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="2e9e1-204">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-204">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2e9e1-205">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2e9e1-205">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
