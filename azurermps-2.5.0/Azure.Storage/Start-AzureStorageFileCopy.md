---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: e12240ed399c458c176ab7e9439752ee6551f190
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786345"
---
# <span data-ttu-id="c4b71-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c4b71-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="c4b71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4b71-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b71-103">Inicia a cópia de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4b71-104">SYNTAX</span></span>

### <span data-ttu-id="c4b71-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="c4b71-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b71-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c4b71-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b71-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="c4b71-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b71-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="c4b71-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b71-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c4b71-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b71-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="c4b71-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b71-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="c4b71-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b71-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="c4b71-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4b71-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="c4b71-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b71-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="c4b71-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4b71-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4b71-115">DESCRIPTION</span></span>
<span data-ttu-id="c4b71-116">O cmdlet **Start-AzureStorageFileCopy** inicia a cópia de um arquivo de origem para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c4b71-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="c4b71-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4b71-117">EXAMPLES</span></span>

### <span data-ttu-id="c4b71-118">Exemplo 1: iniciar a operação de cópia de um arquivo em um arquivo usando o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="c4b71-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="c4b71-119">Esse comando inicia uma operação de cópia de arquivo em arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4b71-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="c4b71-120">O comando especifica o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="c4b71-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="c4b71-121">Exemplo 2: iniciar a operação de cópia do blob para o arquivo usando o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="c4b71-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="c4b71-122">Esse comando inicia uma operação de cópia de BLOB para arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4b71-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="c4b71-123">O comando especifica o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="c4b71-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="c4b71-124">OS</span><span class="sxs-lookup"><span data-stu-id="c4b71-124">PARAMETERS</span></span>

### <span data-ttu-id="c4b71-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="c4b71-125">-AbsoluteUri</span></span>
<span data-ttu-id="c4b71-126">Especifica o URI do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="c4b71-127">Se o local de origem exigir uma credencial, você deve fornecer uma.</span><span class="sxs-lookup"><span data-stu-id="c4b71-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c4b71-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c4b71-129">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c4b71-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c4b71-130">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c4b71-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c4b71-131">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c4b71-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c4b71-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c4b71-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c4b71-133">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c4b71-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c4b71-134">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c4b71-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c4b71-135">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c4b71-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c4b71-136">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c4b71-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c4b71-137">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c4b71-137">The default value is 10.</span></span>

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

### <span data-ttu-id="c4b71-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c4b71-138">-Context</span></span>
<span data-ttu-id="c4b71-139">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b71-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c4b71-140">Para obter um contexto, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c4b71-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b71-141">-DefaultProfile</span></span>
<span data-ttu-id="c4b71-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b71-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4b71-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="c4b71-143">-DestContext</span></span>
<span data-ttu-id="c4b71-144">Especifica o contexto de armazenamento do Azure do destino.</span><span class="sxs-lookup"><span data-stu-id="c4b71-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="c4b71-145">Para obter um contexto, use **New-AzureStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="c4b71-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-146">-Destfile</span><span class="sxs-lookup"><span data-stu-id="c4b71-146">-DestFile</span></span>
<span data-ttu-id="c4b71-147">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="c4b71-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c4b71-148">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c4b71-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="c4b71-149">-DestFilePath</span></span>
<span data-ttu-id="c4b71-150">Especifica o caminho do arquivo de destino relativo ao compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="c4b71-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="c4b71-151">-DestShareName</span></span>
<span data-ttu-id="c4b71-152">Especifica o nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="c4b71-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-153">-Force</span><span class="sxs-lookup"><span data-stu-id="c4b71-153">-Force</span></span>
<span data-ttu-id="c4b71-154">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4b71-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4b71-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c4b71-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c4b71-156">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c4b71-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c4b71-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="c4b71-157">-SrcBlob</span></span>
<span data-ttu-id="c4b71-158">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="c4b71-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="c4b71-159">Você pode criar um blob de nuvem ou obter um usando o cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="c4b71-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="c4b71-160">-SrcBlobName</span></span>
<span data-ttu-id="c4b71-161">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="c4b71-162">-SrcContainer</span></span>
<span data-ttu-id="c4b71-163">Especifica um objeto contêiner de blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="c4b71-164">Você pode criar um objeto contêiner de blob de nuvem ou usar o cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="c4b71-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="c4b71-165">-SrcContainerName</span></span>
<span data-ttu-id="c4b71-166">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="c4b71-167">-SrcFile</span></span>
<span data-ttu-id="c4b71-168">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="c4b71-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c4b71-169">Você pode criar um arquivo de nuvem ou obter um usando **Get-AzureStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="c4b71-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="c4b71-170">-SrcFilePath</span></span>
<span data-ttu-id="c4b71-171">Especifica o caminho do arquivo de origem relativo ao diretório de origem ou ao compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="c4b71-172">-SrcShare</span></span>
<span data-ttu-id="c4b71-173">Especifica um objeto de compartilhamento de arquivo na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="c4b71-174">Você pode criar um compartilhamento de arquivos na nuvem ou obter um usando o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c4b71-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="c4b71-175">-SrcShareName</span></span>
<span data-ttu-id="c4b71-176">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="c4b71-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b71-177">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4b71-177">-Confirm</span></span>
<span data-ttu-id="c4b71-178">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b71-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b71-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b71-179">-WhatIf</span></span>
<span data-ttu-id="c4b71-180">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4b71-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b71-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4b71-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b71-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b71-182">CommonParameters</span></span>
<span data-ttu-id="c4b71-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b71-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b71-184">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b71-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b71-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4b71-185">INPUTS</span></span>

### <span data-ttu-id="c4b71-186">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c4b71-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c4b71-187">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="c4b71-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="c4b71-188">Parâmetros: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4b71-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="c4b71-189">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4b71-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c4b71-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4b71-190">OUTPUTS</span></span>

### <span data-ttu-id="c4b71-191">System. void</span><span class="sxs-lookup"><span data-stu-id="c4b71-191">System.Void</span></span>

## <span data-ttu-id="c4b71-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4b71-192">NOTES</span></span>

## <span data-ttu-id="c4b71-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4b71-193">RELATED LINKS</span></span>

[<span data-ttu-id="c4b71-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c4b71-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="c4b71-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c4b71-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="c4b71-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c4b71-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c4b71-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c4b71-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c4b71-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c4b71-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="c4b71-199">Parar-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c4b71-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
