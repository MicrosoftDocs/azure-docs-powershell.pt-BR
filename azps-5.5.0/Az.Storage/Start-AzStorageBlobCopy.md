---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116090"
---
# <span data-ttu-id="9e4a6-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9e4a6-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="9e4a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4a6-103">Começa a copiar um blob.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="9e4a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e4a6-104">SYNTAX</span></span>

### <span data-ttu-id="9e4a6-105">Nomedo Contêiner (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e4a6-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-107">BlobInstanceToB ltdainstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9e4a6-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-113">FileInstanceToBlhoInstance</span><span class="sxs-lookup"><span data-stu-id="9e4a6-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4a6-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="9e4a6-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e4a6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e4a6-115">DESCRIPTION</span></span>
<span data-ttu-id="9e4a6-116">O cmdlet **Start-AzStorageBcopy começa** a copiar um blob.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="9e4a6-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e4a6-117">EXAMPLES</span></span>

### <span data-ttu-id="9e4a6-118">Exemplo 1: Copiar um blob nomeado</span><span class="sxs-lookup"><span data-stu-id="9e4a6-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="9e4a6-119">Esse comando inicia a operação de cópia do blob chamado ContosoPlanning2015 do contêiner chamado ContosoUploads para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="9e4a6-120">Exemplo 2: Obter um contêiner para especificar blobs a copiar</span><span class="sxs-lookup"><span data-stu-id="9e4a6-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="9e4a6-121">Esse comando obtém o contêiner chamado ContosoUploads usando o cmdlet **Get-AzStorageContainer** e passa o contêiner para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e4a6-122">Esse cmdlet inicia a operação de cópia do blob chamado ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="9e4a6-123">O cmdlet anterior fornece o contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="9e4a6-124">O *parâmetro DestContainer* especifica ContosoArchives como o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="9e4a6-125">Exemplo 3: Obter todos os blobs em um contêiner e copiá-los</span><span class="sxs-lookup"><span data-stu-id="9e4a6-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="9e4a6-126">Esse comando obtém os blobs no contêiner chamado ContosoUploads, usando o cmdlet **Get-AzStorageB ltd** e, em seguida, passa os resultados para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e4a6-127">Esse cmdlet inicia a operação de cópia dos blobs para o contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="9e4a6-128">Exemplo 4: Copiar um blob especificado como um objeto</span><span class="sxs-lookup"><span data-stu-id="9e4a6-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="9e4a6-129">O primeiro comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="9e4a6-130">O comando armazena esse objeto na variável $SrcBlob dados.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="9e4a6-131">O segundo comando obtém o blob chamado ContosoPlanning2015Archived no contêiner chamado ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="9e4a6-132">O comando armazena esse objeto na variável $DestBlob dados.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="9e4a6-133">O último comando inicia a operação de cópia do contêiner de origem para o contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="9e4a6-134">O comando usa notação de ponto padrão para especificar os objetos **ICloudBcloud** para $SrcBlob e $DestBlob blobs.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="9e4a6-135">Exemplo 5: Copiar um blob de um URI</span><span class="sxs-lookup"><span data-stu-id="9e4a6-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="9e4a6-136">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e armazena essa chave na variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="9e4a6-137">O segundo comando copia o arquivo do URI especificado para o blob chamado ContosoPlanning no contêiner chamado ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="9e4a6-138">O comando inicia a operação de cópia para o contexto de destino armazenado $Context.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="9e4a6-139">Não há contexto de armazenamento de origem, portanto, o Uri de origem deve ter acesso ao objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="9e4a6-140">Por exemplo: se a fonte for um blob do Azure público, o Uri deverá conter um token SAS que tenha acesso de leitura ao blob.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="9e4a6-141">Exemplo 6: Copiar um blob de bloco para o contêiner de destino com um novo nome de blob e definir o blob de destino StandardBtier como Hot, ReateatePriority como Alto</span><span class="sxs-lookup"><span data-stu-id="9e4a6-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="9e4a6-142">Esse comando inicia a operação de cópia de um blob de bloco no contêiner de destino com um novo nome de blob e desfaixa o blob de destino StandardBtier como Hot, ReateatePriority como Alto</span><span class="sxs-lookup"><span data-stu-id="9e4a6-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="9e4a6-143">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e4a6-143">PARAMETERS</span></span>

### <span data-ttu-id="9e4a6-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="9e4a6-144">-AbsoluteUri</span></span>
<span data-ttu-id="9e4a6-145">Especifica o URI absoluto de um arquivo a ser copiado para um blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="9e4a6-146">-BlobBaseClient</span></span>
<span data-ttu-id="9e4a6-147">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="9e4a6-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e4a6-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e4a6-149">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9e4a6-150">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9e4a6-151">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e4a6-152">-CloudBlab</span><span class="sxs-lookup"><span data-stu-id="9e4a6-152">-CloudBlob</span></span>
<span data-ttu-id="9e4a6-153">Especifica um objeto **CloudB object** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="9e4a6-154">Para obter um **objeto CloudB ltd,** use o cmdlet Get-AzStorageBlob nuvem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-155">-CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="9e4a6-155">-CloudBlobContainer</span></span>
<span data-ttu-id="9e4a6-156">Especifica um objeto **CloudBltContainer** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9e4a6-157">Este cmdlet copia um blob do contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="9e4a6-158">Para obter um **objeto CloudBltContainer,** use o cmdlet Get-AzStorageContainer nuvem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e4a6-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e4a6-160">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9e4a6-161">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9e4a6-162">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9e4a6-163">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9e4a6-164">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-164">The default value is 10.</span></span>

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

### <span data-ttu-id="9e4a6-165">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9e4a6-165">-Context</span></span>
<span data-ttu-id="9e4a6-166">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e4a6-167">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4a6-168">-DefaultProfile</span></span>
<span data-ttu-id="9e4a6-169">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4a6-170">-DestB meteor</span><span class="sxs-lookup"><span data-stu-id="9e4a6-170">-DestBlob</span></span>
<span data-ttu-id="9e4a6-171">Especifica o nome do blob de destino.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-172">-DestCloudBcloudBcloud</span><span class="sxs-lookup"><span data-stu-id="9e4a6-172">-DestCloudBlob</span></span>
<span data-ttu-id="9e4a6-173">Especifica um objeto **CloudB ltd de** destino</span><span class="sxs-lookup"><span data-stu-id="9e4a6-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="9e4a6-174">-DestContainer</span></span>
<span data-ttu-id="9e4a6-175">Especifica o nome do contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="9e4a6-176">-DestContext</span></span>
<span data-ttu-id="9e4a6-177">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e4a6-178">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-179">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9e4a6-179">-Force</span></span>
<span data-ttu-id="9e4a6-180">Indica que esse cmdlet substitui o blob de destino sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9e4a6-181">-PremiumPageBtier</span><span class="sxs-lookup"><span data-stu-id="9e4a6-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="9e4a6-182">Camada de Blob de Página Premium</span><span class="sxs-lookup"><span data-stu-id="9e4a6-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-183">-ReatarPrioridade</span><span class="sxs-lookup"><span data-stu-id="9e4a6-183">-RehydratePriority</span></span>
<span data-ttu-id="9e4a6-184">Bloquear Blob ReateatePriority.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="9e4a6-185">Indica a prioridade com a qual reatear um blob arquivado.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="9e4a6-186">Os valores válidos são Alto/Padrão.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e4a6-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e4a6-188">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9e4a6-189">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9e4a6-190">-SrcB cdc</span><span class="sxs-lookup"><span data-stu-id="9e4a6-190">-SrcBlob</span></span>
<span data-ttu-id="9e4a6-191">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="9e4a6-192">-SrcContainer</span></span>
<span data-ttu-id="9e4a6-193">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="9e4a6-194">-SrcDir</span></span>
<span data-ttu-id="9e4a6-195">Especifica um objeto **CloudFileDirectory** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="9e4a6-196">-SrcFile</span></span>
<span data-ttu-id="9e4a6-197">Especifica um objeto **CloudFile** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="9e4a6-198">Você pode criar ou usar Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="9e4a6-199">-SrcFilePath</span></span>
<span data-ttu-id="9e4a6-200">Especifica o caminho relativo do arquivo de origem do diretório de origem ou do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="9e4a6-201">-SrcShare</span></span>
<span data-ttu-id="9e4a6-202">Especifica um objeto **CloudFileShare** da biblioteca do Cliente de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="9e4a6-203">Você pode criar ou usar Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="9e4a6-204">-SrcShareName</span></span>
<span data-ttu-id="9e4a6-205">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4a6-206">-StandardBtier</span><span class="sxs-lookup"><span data-stu-id="9e4a6-206">-StandardBlobTier</span></span>
<span data-ttu-id="9e4a6-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="9e4a6-208">Ver detalhes em https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="9e4a6-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="9e4a6-209">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9e4a6-209">-Confirm</span></span>
<span data-ttu-id="9e4a6-210">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4a6-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4a6-211">-WhatIf</span></span>
<span data-ttu-id="9e4a6-212">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e4a6-213">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4a6-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4a6-214">CommonParameters</span></span>
<span data-ttu-id="9e4a6-215">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4a6-216">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4a6-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4a6-217">Entradas</span><span class="sxs-lookup"><span data-stu-id="9e4a6-217">INPUTS</span></span>

### <span data-ttu-id="9e4a6-218">Microsoft.Azure.Storage.Blob.CloudBlab</span><span class="sxs-lookup"><span data-stu-id="9e4a6-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9e4a6-219">Microsoft.Azure.Storage.Blob.CloudBltContainer</span><span class="sxs-lookup"><span data-stu-id="9e4a6-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9e4a6-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="9e4a6-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="9e4a6-221">System.String</span><span class="sxs-lookup"><span data-stu-id="9e4a6-221">System.String</span></span>

### <span data-ttu-id="9e4a6-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e4a6-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e4a6-223">Saídas</span><span class="sxs-lookup"><span data-stu-id="9e4a6-223">OUTPUTS</span></span>

### <span data-ttu-id="9e4a6-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlab</span><span class="sxs-lookup"><span data-stu-id="9e4a6-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9e4a6-225">Notas</span><span class="sxs-lookup"><span data-stu-id="9e4a6-225">NOTES</span></span>

## <span data-ttu-id="9e4a6-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e4a6-226">RELATED LINKS</span></span>

[<span data-ttu-id="9e4a6-227">Get-AzStorageBcopyState</span><span class="sxs-lookup"><span data-stu-id="9e4a6-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="9e4a6-228">Stop-AzStorageBcopy</span><span class="sxs-lookup"><span data-stu-id="9e4a6-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
