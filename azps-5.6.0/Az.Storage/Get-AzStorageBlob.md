---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 317d25ecfa48203c411f368aa5b00ac3380773ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891997"
---
# <span data-ttu-id="5b526-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5b526-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="5b526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b526-102">SYNOPSIS</span></span>
<span data-ttu-id="5b526-103">Lista blobs em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="5b526-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="5b526-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5b526-104">SYNTAX</span></span>

### <span data-ttu-id="5b526-105">BlobName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b526-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b526-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5b526-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5b526-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="5b526-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5b526-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="5b526-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5b526-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5b526-109">DESCRIPTION</span></span>
<span data-ttu-id="5b526-110">O cmdlet **Get-AzStorageBlob** lista blobs no contêiner especificado em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5b526-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="5b526-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b526-111">EXAMPLES</span></span>

### <span data-ttu-id="5b526-112">Exemplo 1: Obter um blob por nome de blob</span><span class="sxs-lookup"><span data-stu-id="5b526-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="5b526-113">Este comando usa um nome de blob e um caractere curinga para obter um blob.</span><span class="sxs-lookup"><span data-stu-id="5b526-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="5b526-114">Exemplo 2: Obter blobs em um contêiner usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="5b526-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="5b526-115">Este comando usa o pipeline para obter todos os blobs (incluir blobs no status excluído) em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="5b526-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="5b526-116">Exemplo 3: Obter blobs por prefixo de nome</span><span class="sxs-lookup"><span data-stu-id="5b526-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="5b526-117">Este comando usa um prefixo de nome para obter blobs.</span><span class="sxs-lookup"><span data-stu-id="5b526-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="5b526-118">Exemplo 4: listar blobs em vários lotes</span><span class="sxs-lookup"><span data-stu-id="5b526-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="5b526-119">Este exemplo usa os *parâmetros MaxCount* e *ContinuationToken* para listar blobs de Armazenamento do Azure em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="5b526-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="5b526-120">Os quatro primeiros comandos atribuem valores a variáveis a ser usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="5b526-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="5b526-121">O quinto comando especifica uma instrução **Do-While** que usa o cmdlet **Get-AzStorageBlob** para obter blobs.</span><span class="sxs-lookup"><span data-stu-id="5b526-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="5b526-122">A instrução inclui o token de continuação armazenado na variável $Token.</span><span class="sxs-lookup"><span data-stu-id="5b526-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="5b526-123">$Token altera o valor à medida que o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="5b526-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="5b526-124">Para obter mais informações, digite `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="5b526-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="5b526-125">O comando final usa o **comando Echo** para exibir o total.</span><span class="sxs-lookup"><span data-stu-id="5b526-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="5b526-126">Exemplo 5: Obter todos os blobs em um contêiner incluem a versão blob</span><span class="sxs-lookup"><span data-stu-id="5b526-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="5b526-127">Este comando obtém todos os blobs em um contêiner incluem a versão de blob.</span><span class="sxs-lookup"><span data-stu-id="5b526-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="5b526-128">Exemplo 6: Obter uma única versão de blob</span><span class="sxs-lookup"><span data-stu-id="5b526-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="5b526-129">Este comando obtém um único vértice de blobs com VersionId.</span><span class="sxs-lookup"><span data-stu-id="5b526-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="5b526-130">Exemplo 7: Obter um único instantâneo de blob</span><span class="sxs-lookup"><span data-stu-id="5b526-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="5b526-131">Este comando obtém um único instantâneo de blobs com InstantâneoTime.</span><span class="sxs-lookup"><span data-stu-id="5b526-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="5b526-132">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5b526-132">PARAMETERS</span></span>

### <span data-ttu-id="5b526-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="5b526-133">-Blob</span></span>
<span data-ttu-id="5b526-134">Especifica um nome ou padrão de nome, que pode ser usado para uma pesquisa de caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="5b526-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="5b526-135">Se nenhum nome de blob for especificado, o cmdlet lista todos os blobs no contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="5b526-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="5b526-136">Se um valor for especificado para esse parâmetro, o cmdlet lista todos os blobs com nomes que corresponderem a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5b526-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="5b526-137">Este parâmetro dá suporte a caracteres curinga em qualquer lugar na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5b526-137">This parameter supports wildcards anywhere in the string.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b526-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b526-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5b526-139">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="5b526-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5b526-140">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b526-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5b526-141">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5b526-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5b526-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5b526-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5b526-143">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5b526-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5b526-144">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5b526-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5b526-145">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="5b526-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5b526-146">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="5b526-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5b526-147">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="5b526-147">The default value is 10.</span></span>

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

### <span data-ttu-id="5b526-148">-Container</span><span class="sxs-lookup"><span data-stu-id="5b526-148">-Container</span></span>
<span data-ttu-id="5b526-149">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="5b526-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="5b526-150">-Context</span><span class="sxs-lookup"><span data-stu-id="5b526-150">-Context</span></span>
<span data-ttu-id="5b526-151">Especifica a conta de armazenamento do Azure da qual você deseja obter uma lista de blobs.</span><span class="sxs-lookup"><span data-stu-id="5b526-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="5b526-152">Você pode usar o cmdlet New-AzStorageContext para criar um contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5b526-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="5b526-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="5b526-153">-ContinuationToken</span></span>
<span data-ttu-id="5b526-154">Especifica um token de continuação para a lista de blob.</span><span class="sxs-lookup"><span data-stu-id="5b526-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="5b526-155">Use esse parâmetro e o *parâmetro MaxCount* para listar blobs em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="5b526-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b526-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b526-156">-DefaultProfile</span></span>
<span data-ttu-id="5b526-157">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b526-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b526-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="5b526-158">-IncludeDeleted</span></span>
<span data-ttu-id="5b526-159">Incluir Blob Excluído, por padrão, obter blob não incluirá blob excluído.</span><span class="sxs-lookup"><span data-stu-id="5b526-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="5b526-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="5b526-160">-IncludeVersion</span></span>
<span data-ttu-id="5b526-161">As versões de blob serão listadas somente se esse parâmetro estiver presente, por padrão obter blob não incluirá versões blob.</span><span class="sxs-lookup"><span data-stu-id="5b526-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b526-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5b526-162">-MaxCount</span></span>
<span data-ttu-id="5b526-163">Especifica o número máximo de objetos que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="5b526-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="5b526-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5b526-164">-Prefix</span></span>
<span data-ttu-id="5b526-165">Especifica um prefixo para os nomes de blob que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="5b526-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="5b526-166">Esse parâmetro não dá suporte ao uso de expressões regulares ou caracteres curinga para pesquisar.</span><span class="sxs-lookup"><span data-stu-id="5b526-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="5b526-167">Isso significa que, se o contêiner tiver apenas blobs chamados "My", "MyBlob1" e "MyBlob2" e você especificar "-Prefix My\*", o cmdlet não retornará blobs.</span><span class="sxs-lookup"><span data-stu-id="5b526-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="5b526-168">No entanto, se você especificar "-Prefix My", o cmdlet retornará "My", "MyBlob1" e "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="5b526-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="5b526-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b526-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5b526-170">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b526-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="5b526-171">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5b526-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="5b526-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5b526-172">-SnapshotTime</span></span>
<span data-ttu-id="5b526-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5b526-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b526-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="5b526-174">-VersionId</span></span>
<span data-ttu-id="5b526-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="5b526-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b526-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b526-176">CommonParameters</span></span>
<span data-ttu-id="5b526-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b526-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b526-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b526-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b526-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b526-179">INPUTS</span></span>

### <span data-ttu-id="5b526-180">System.String</span><span class="sxs-lookup"><span data-stu-id="5b526-180">System.String</span></span>

### <span data-ttu-id="5b526-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b526-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b526-182">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5b526-182">OUTPUTS</span></span>

### <span data-ttu-id="5b526-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5b526-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="5b526-184">NOTES</span><span class="sxs-lookup"><span data-stu-id="5b526-184">NOTES</span></span>

## <span data-ttu-id="5b526-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b526-185">RELATED LINKS</span></span>

[<span data-ttu-id="5b526-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b526-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="5b526-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5b526-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="5b526-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b526-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


