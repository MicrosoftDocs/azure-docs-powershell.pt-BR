---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427687"
---
# <span data-ttu-id="67355-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="67355-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="67355-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67355-102">SYNOPSIS</span></span>
<span data-ttu-id="67355-103">Carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="67355-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="67355-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67355-104">SYNTAX</span></span>

### <span data-ttu-id="67355-105">SendManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="67355-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67355-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="67355-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67355-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="67355-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67355-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67355-108">DESCRIPTION</span></span>
<span data-ttu-id="67355-109">O cmdlet **set-AzStorageBlobContent** carrega um arquivo local em um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="67355-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="67355-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67355-110">EXAMPLES</span></span>

### <span data-ttu-id="67355-111">Exemplo 1: carregar um arquivo nomeado</span><span class="sxs-lookup"><span data-stu-id="67355-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="67355-112">Esse comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.</span><span class="sxs-lookup"><span data-stu-id="67355-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="67355-113">Exemplo 2: carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="67355-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="67355-114">Esse comando usa o cmdlet principal do Windows PowerShell Get-ChildItem para obter todos os arquivos na pasta atual e em subpastas e, em seguida, passá-los para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="67355-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="67355-115">O cmdlet **set-AzStorageBlobContent** carrega os arquivos para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="67355-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="67355-116">Exemplo 3: substituir um blob existente</span><span class="sxs-lookup"><span data-stu-id="67355-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="67355-117">Esse comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzStorageBlob e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="67355-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="67355-118">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="67355-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="67355-119">Esse comando não especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="67355-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="67355-120">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="67355-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="67355-121">Se você confirmar o comando, o cmdlet substituirá o blob existente.</span><span class="sxs-lookup"><span data-stu-id="67355-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="67355-122">Exemplo 4: carregar um arquivo em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="67355-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="67355-123">Esse comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="67355-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="67355-124">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="67355-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="67355-125">Exemplo 5: carregar um arquivo no BLOB da página com metadados e PremiumPageBlobTier como P10</span><span class="sxs-lookup"><span data-stu-id="67355-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="67355-126">O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na variável $Metadata.</span><span class="sxs-lookup"><span data-stu-id="67355-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="67355-127">O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="67355-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="67355-128">O blob inclui os metadados armazenados no $Metadata e tem PremiumPageBlobTier como P10.</span><span class="sxs-lookup"><span data-stu-id="67355-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="67355-129">Exemplo 6: carregar um arquivo para blob com propriedades de blob especificadas e definir StandardBlobTier como legal</span><span class="sxs-lookup"><span data-stu-id="67355-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="67355-130">Esse comando carrega o arquivo c:\temp\index.html para o contêiner chamado contosouploads com as propriedades de blob especificadas e define StandardBlobTier como legal.</span><span class="sxs-lookup"><span data-stu-id="67355-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="67355-131">Esse comando obtém o valor ContentType definido como propriedades de blob por [System. Web. MimeMapping]:: GetMimeMapping () API.</span><span class="sxs-lookup"><span data-stu-id="67355-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="67355-132">Exemplo 7: carregar um arquivo em um blob com escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="67355-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="67355-133">Esse comando carrega um arquivo em um blob com escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="67355-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="67355-134">OS</span><span class="sxs-lookup"><span data-stu-id="67355-134">PARAMETERS</span></span>

### <span data-ttu-id="67355-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67355-135">-AsJob</span></span>
<span data-ttu-id="67355-136">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="67355-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="67355-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="67355-137">-Blob</span></span>
<span data-ttu-id="67355-138">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="67355-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="67355-139">Esse cmdlet carrega um arquivo para o blob de armazenamento do Azure que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="67355-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="67355-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="67355-140">-BlobType</span></span>
<span data-ttu-id="67355-141">Especifica o tipo do blob que esse cmdlet carregará.</span><span class="sxs-lookup"><span data-stu-id="67355-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="67355-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="67355-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="67355-143">Block</span><span class="sxs-lookup"><span data-stu-id="67355-143">Block</span></span>
- <span data-ttu-id="67355-144">Page</span><span class="sxs-lookup"><span data-stu-id="67355-144">Page</span></span>
- <span data-ttu-id="67355-145">Acrescentar o valor padrão é bloquear.</span><span class="sxs-lookup"><span data-stu-id="67355-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="67355-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="67355-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="67355-147">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="67355-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="67355-148">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="67355-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="67355-149">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="67355-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="67355-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="67355-150">-CloudBlob</span></span>
<span data-ttu-id="67355-151">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="67355-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="67355-152">Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="67355-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="67355-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="67355-153">-CloudBlobContainer</span></span>
<span data-ttu-id="67355-154">Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="67355-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="67355-155">Esse cmdlet carrega o conteúdo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="67355-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="67355-156">Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="67355-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="67355-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="67355-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="67355-158">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="67355-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="67355-159">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="67355-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="67355-160">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="67355-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="67355-161">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="67355-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="67355-162">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="67355-162">The default value is 10.</span></span>

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

### <span data-ttu-id="67355-163">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="67355-163">-Container</span></span>
<span data-ttu-id="67355-164">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="67355-164">Specifies the name of a container.</span></span>
<span data-ttu-id="67355-165">Esse cmdlet carrega um arquivo em um blob no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="67355-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="67355-166">-Contexto</span><span class="sxs-lookup"><span data-stu-id="67355-166">-Context</span></span>
<span data-ttu-id="67355-167">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="67355-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="67355-168">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="67355-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="67355-169">Para usar um contexto de armazenamento criado a partir de um token SAS sem permissão de leitura, é preciso ter o parâmetro Add-Force para ignorar a existência da verificação de BLOB.</span><span class="sxs-lookup"><span data-stu-id="67355-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="67355-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67355-170">-DefaultProfile</span></span>
<span data-ttu-id="67355-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67355-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67355-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="67355-172">-EncryptionScope</span></span>
<span data-ttu-id="67355-173">Escopo de criptografia a ser usado ao fazer solicitações ao blob.</span><span class="sxs-lookup"><span data-stu-id="67355-173">Encryption scope to be used when making requests to the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67355-174">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="67355-174">-File</span></span>
<span data-ttu-id="67355-175">Especifica um caminho de arquivo local para o carregamento de um arquivo como conteúdo BLOB.</span><span class="sxs-lookup"><span data-stu-id="67355-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="67355-176">-Force</span><span class="sxs-lookup"><span data-stu-id="67355-176">-Force</span></span>
<span data-ttu-id="67355-177">Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="67355-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="67355-178">-Metadados</span><span class="sxs-lookup"><span data-stu-id="67355-178">-Metadata</span></span>
<span data-ttu-id="67355-179">Especifica metadados para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="67355-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="67355-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="67355-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="67355-181">Camada de blob de página</span><span class="sxs-lookup"><span data-stu-id="67355-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="67355-182">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="67355-182">-Properties</span></span>
<span data-ttu-id="67355-183">Especifica as propriedades do blob carregado.</span><span class="sxs-lookup"><span data-stu-id="67355-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="67355-184">As propriedades com suporte são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="67355-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="67355-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="67355-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="67355-186">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="67355-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="67355-187">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="67355-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="67355-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="67355-188">-StandardBlobTier</span></span>
<span data-ttu-id="67355-189">Camada de bloco de BLOB, os valores válidos são quente/interessante/arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="67355-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="67355-190">Veja detalhes em https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="67355-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="67355-191">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67355-191">-Confirm</span></span>
<span data-ttu-id="67355-192">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67355-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67355-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67355-193">-WhatIf</span></span>
<span data-ttu-id="67355-194">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67355-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67355-195">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67355-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67355-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67355-196">CommonParameters</span></span>
<span data-ttu-id="67355-197">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67355-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67355-198">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67355-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67355-199">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67355-199">INPUTS</span></span>

### <span data-ttu-id="67355-200">System. String</span><span class="sxs-lookup"><span data-stu-id="67355-200">System.String</span></span>

### <span data-ttu-id="67355-201">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="67355-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="67355-202">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="67355-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="67355-203">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="67355-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="67355-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67355-204">OUTPUTS</span></span>

### <span data-ttu-id="67355-205">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="67355-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="67355-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67355-206">NOTES</span></span>

## <span data-ttu-id="67355-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67355-207">RELATED LINKS</span></span>

[<span data-ttu-id="67355-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="67355-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="67355-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="67355-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="67355-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="67355-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
