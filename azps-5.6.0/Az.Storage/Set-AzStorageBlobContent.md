---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 66cad13b7c3b1596b2ce369b454f5a0f9ff54b8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888406"
---
# <span data-ttu-id="6ab9d-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ab9d-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="6ab9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab9d-103">Carrega um arquivo local em um blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="6ab9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ab9d-104">SYNTAX</span></span>

### <span data-ttu-id="6ab9d-105">SendManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6ab9d-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab9d-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6ab9d-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab9d-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6ab9d-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab9d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ab9d-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab9d-109">O cmdlet **Set-AzStorageBlobContent** carrega um arquivo local para um blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="6ab9d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab9d-111">Exemplo 1: Carregar um arquivo nomeado</span><span class="sxs-lookup"><span data-stu-id="6ab9d-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="6ab9d-112">Este comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="6ab9d-113">Exemplo 2: Carregar todos os arquivos na pasta atual</span><span class="sxs-lookup"><span data-stu-id="6ab9d-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="6ab9d-114">Este comando usa o núcleo Windows PowerShell cmdlet Get-ChildItem para obter todos os arquivos na pasta atual e nas subpastas e, em seguida, os passa para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ab9d-115">O cmdlet **Set-AzStorageBlobContent** carrega os arquivos no contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="6ab9d-116">Exemplo 3: substituir um blob existente</span><span class="sxs-lookup"><span data-stu-id="6ab9d-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="6ab9d-117">Este comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzStorageBlob e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="6ab9d-118">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="6ab9d-119">Este comando não especifica o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="6ab9d-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="6ab9d-120">O comando solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6ab9d-121">Se você confirmar o comando, o cmdlet substituirá o blob existente.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="6ab9d-122">Exemplo 4: Carregar um arquivo em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="6ab9d-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="6ab9d-123">Este comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="6ab9d-124">O comando carrega o arquivo chamado ContosoPlanning como Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="6ab9d-125">Exemplo 5: Carregar um arquivo para blob de página com metadados e PremiumPageBlobTier como P10</span><span class="sxs-lookup"><span data-stu-id="6ab9d-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="6ab9d-126">O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na $Metadata variável.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="6ab9d-127">O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="6ab9d-128">O blob inclui os metadados armazenados no $Metadata e tem PremiumPageBlobTier como P10.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="6ab9d-129">Exemplo 6: Carregar um arquivo para blob com propriedades de blob especificadas e definir StandardBlobTier como Cool</span><span class="sxs-lookup"><span data-stu-id="6ab9d-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="6ab9d-130">Este comando carrega o arquivo c:\temp\index.html para o contêiner chamado contosouploads com propriedades de blob especificadas e define StandardBlobTier como Cool.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="6ab9d-131">Este comando obtém o valor ContentType definido como propriedades blob por [System.Web.MimeMapping]::GetMimeMapping() API.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="6ab9d-132">Exemplo 7: Carregar um arquivo em um blob com escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="6ab9d-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="6ab9d-133">Este comando carrega um arquivo em um blob com Escopo de Criptografia.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="6ab9d-134">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-134">PARAMETERS</span></span>

### <span data-ttu-id="6ab9d-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-135">-AsJob</span></span>
<span data-ttu-id="6ab9d-136">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6ab9d-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-137">-Blob</span></span>
<span data-ttu-id="6ab9d-138">Especifica o nome de um blob.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="6ab9d-139">Este cmdlet carrega um arquivo no blob armazenamento do Azure especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ab9d-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="6ab9d-140">-BlobType</span></span>
<span data-ttu-id="6ab9d-141">Especifica o tipo para o blob que esse cmdlet carrega.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="6ab9d-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6ab9d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ab9d-143">Bloquear</span><span class="sxs-lookup"><span data-stu-id="6ab9d-143">Block</span></span>
- <span data-ttu-id="6ab9d-144">Page</span><span class="sxs-lookup"><span data-stu-id="6ab9d-144">Page</span></span>
- <span data-ttu-id="6ab9d-145">Anexar O valor padrão é Block.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="6ab9d-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ab9d-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ab9d-147">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ab9d-148">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ab9d-149">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ab9d-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-150">-CloudBlob</span></span>
<span data-ttu-id="6ab9d-151">Especifica um **objeto CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="6ab9d-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="6ab9d-152">Para obter um **objeto CloudBlob,** use Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6ab9d-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ab9d-153">-CloudBlobContainer</span></span>
<span data-ttu-id="6ab9d-154">Especifica um **objeto CloudBlobContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6ab9d-155">Este cmdlet carrega conteúdo em um blob no contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="6ab9d-156">Para obter um **objeto CloudBlobContainer,** use Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6ab9d-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ab9d-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ab9d-158">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ab9d-159">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ab9d-160">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ab9d-161">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ab9d-162">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-162">The default value is 10.</span></span>

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

### <span data-ttu-id="6ab9d-163">-Container</span><span class="sxs-lookup"><span data-stu-id="6ab9d-163">-Container</span></span>
<span data-ttu-id="6ab9d-164">Especifica o nome de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-164">Specifies the name of a container.</span></span>
<span data-ttu-id="6ab9d-165">Este cmdlet carrega um arquivo em um blob no contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ab9d-166">-Context</span><span class="sxs-lookup"><span data-stu-id="6ab9d-166">-Context</span></span>
<span data-ttu-id="6ab9d-167">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ab9d-168">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="6ab9d-169">Para usar um contexto de armazenamento criado a partir de um Token SAS sem permissão de leitura, é necessário adicionar parâmetro -Force para ignorar a existência de blob de verificação.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="6ab9d-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab9d-170">-DefaultProfile</span></span>
<span data-ttu-id="6ab9d-171">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab9d-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6ab9d-172">-EncryptionScope</span></span>
<span data-ttu-id="6ab9d-173">Escopo de criptografia a ser usado ao fazer solicitações ao blob.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="6ab9d-174">-File</span><span class="sxs-lookup"><span data-stu-id="6ab9d-174">-File</span></span>
<span data-ttu-id="6ab9d-175">Especifica um caminho de arquivo local para um arquivo carregar como conteúdo blob.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="6ab9d-176">-Force</span><span class="sxs-lookup"><span data-stu-id="6ab9d-176">-Force</span></span>
<span data-ttu-id="6ab9d-177">Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6ab9d-178">-Metadados</span><span class="sxs-lookup"><span data-stu-id="6ab9d-178">-Metadata</span></span>
<span data-ttu-id="6ab9d-179">Especifica metadados para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="6ab9d-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="6ab9d-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="6ab9d-181">Camada de blob de página</span><span class="sxs-lookup"><span data-stu-id="6ab9d-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="6ab9d-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="6ab9d-182">-Properties</span></span>
<span data-ttu-id="6ab9d-183">Especifica propriedades para o blob carregado.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="6ab9d-184">As propriedades suportadas são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="6ab9d-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ab9d-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ab9d-186">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6ab9d-187">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6ab9d-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6ab9d-188">-StandardBlobTier</span></span>
<span data-ttu-id="6ab9d-189">Bloquear Camada de Blob, os valores válidos são Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6ab9d-190">Confira detalhes em https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6ab9d-190">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="6ab9d-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ab9d-191">-Confirm</span></span>
<span data-ttu-id="6ab9d-192">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab9d-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab9d-193">-WhatIf</span></span>
<span data-ttu-id="6ab9d-194">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab9d-195">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab9d-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab9d-196">CommonParameters</span></span>
<span data-ttu-id="6ab9d-197">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab9d-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab9d-198">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab9d-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab9d-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-199">INPUTS</span></span>

### <span data-ttu-id="6ab9d-200">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab9d-200">System.String</span></span>

### <span data-ttu-id="6ab9d-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ab9d-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6ab9d-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6ab9d-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ab9d-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ab9d-204">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-204">OUTPUTS</span></span>

### <span data-ttu-id="6ab9d-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6ab9d-206">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ab9d-206">NOTES</span></span>

## <span data-ttu-id="6ab9d-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ab9d-207">RELATED LINKS</span></span>

[<span data-ttu-id="6ab9d-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ab9d-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="6ab9d-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6ab9d-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ab9d-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
