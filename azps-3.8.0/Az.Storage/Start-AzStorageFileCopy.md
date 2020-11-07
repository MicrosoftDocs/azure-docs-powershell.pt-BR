---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2cbe08b637808ff782a50f0fa0d50df4bffca73e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941502"
---
# <span data-ttu-id="bd39a-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bd39a-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="bd39a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd39a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd39a-103">Inicia a cópia de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="bd39a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd39a-104">SYNTAX</span></span>

### <span data-ttu-id="bd39a-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="bd39a-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd39a-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bd39a-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="bd39a-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd39a-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="bd39a-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd39a-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="bd39a-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="bd39a-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd39a-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="bd39a-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd39a-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd39a-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd39a-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd39a-115">DESCRIPTION</span></span>
<span data-ttu-id="bd39a-116">O cmdlet **Start-AzStorageFileCopy** inicia a cópia de um arquivo de origem para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="bd39a-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="bd39a-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd39a-117">EXAMPLES</span></span>

### <span data-ttu-id="bd39a-118">Exemplo 1: iniciar a operação de cópia de um arquivo em um arquivo usando o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="bd39a-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="bd39a-119">Esse comando inicia uma operação de cópia de arquivo em arquivo.</span><span class="sxs-lookup"><span data-stu-id="bd39a-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="bd39a-120">O comando especifica o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="bd39a-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="bd39a-121">Exemplo 2: iniciar a operação de cópia do blob para o arquivo usando o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="bd39a-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="bd39a-122">Esse comando inicia uma operação de cópia de BLOB para arquivo.</span><span class="sxs-lookup"><span data-stu-id="bd39a-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="bd39a-123">O comando especifica o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="bd39a-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="bd39a-124">OS</span><span class="sxs-lookup"><span data-stu-id="bd39a-124">PARAMETERS</span></span>

### <span data-ttu-id="bd39a-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="bd39a-125">-AbsoluteUri</span></span>
<span data-ttu-id="bd39a-126">Especifica o URI do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="bd39a-127">Se o local de origem exigir uma credencial, você deve fornecer uma.</span><span class="sxs-lookup"><span data-stu-id="bd39a-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="bd39a-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd39a-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bd39a-129">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="bd39a-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bd39a-130">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd39a-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bd39a-131">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="bd39a-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bd39a-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bd39a-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bd39a-133">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bd39a-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bd39a-134">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="bd39a-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bd39a-135">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="bd39a-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bd39a-136">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bd39a-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bd39a-137">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bd39a-137">The default value is 10.</span></span>

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

### <span data-ttu-id="bd39a-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bd39a-138">-Context</span></span>
<span data-ttu-id="bd39a-139">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd39a-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bd39a-140">Para obter um contexto, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bd39a-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bd39a-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd39a-141">-DefaultProfile</span></span>
<span data-ttu-id="bd39a-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd39a-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd39a-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="bd39a-143">-DestContext</span></span>
<span data-ttu-id="bd39a-144">Especifica o contexto de armazenamento do Azure do destino.</span><span class="sxs-lookup"><span data-stu-id="bd39a-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="bd39a-145">Para obter um contexto, use **New-AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="bd39a-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="bd39a-146">-Destfile</span><span class="sxs-lookup"><span data-stu-id="bd39a-146">-DestFile</span></span>
<span data-ttu-id="bd39a-147">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="bd39a-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="bd39a-148">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="bd39a-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd39a-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="bd39a-149">-DestFilePath</span></span>
<span data-ttu-id="bd39a-150">Especifica o caminho do arquivo de destino relativo ao compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="bd39a-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="bd39a-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="bd39a-151">-DestShareName</span></span>
<span data-ttu-id="bd39a-152">Especifica o nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="bd39a-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="bd39a-153">-Force</span><span class="sxs-lookup"><span data-stu-id="bd39a-153">-Force</span></span>
<span data-ttu-id="bd39a-154">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd39a-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd39a-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd39a-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bd39a-156">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd39a-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bd39a-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="bd39a-157">-SrcBlob</span></span>
<span data-ttu-id="bd39a-158">Especifica um objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="bd39a-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="bd39a-159">Você pode criar um blob de nuvem ou obter um usando o cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="bd39a-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd39a-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="bd39a-160">-SrcBlobName</span></span>
<span data-ttu-id="bd39a-161">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="bd39a-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="bd39a-162">-SrcContainer</span></span>
<span data-ttu-id="bd39a-163">Especifica um objeto contêiner de blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="bd39a-164">Você pode criar um objeto contêiner de blob de nuvem ou usar o cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="bd39a-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd39a-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="bd39a-165">-SrcContainerName</span></span>
<span data-ttu-id="bd39a-166">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="bd39a-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="bd39a-167">-SrcFile</span></span>
<span data-ttu-id="bd39a-168">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="bd39a-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="bd39a-169">Você pode criar um arquivo de nuvem ou obter um usando **Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="bd39a-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd39a-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="bd39a-170">-SrcFilePath</span></span>
<span data-ttu-id="bd39a-171">Especifica o caminho do arquivo de origem relativo ao diretório de origem ou ao compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="bd39a-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="bd39a-172">-SrcShare</span></span>
<span data-ttu-id="bd39a-173">Especifica um objeto de compartilhamento de arquivo na nuvem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="bd39a-174">Você pode criar um compartilhamento de arquivos na nuvem ou obter um usando o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bd39a-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd39a-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="bd39a-175">-SrcShareName</span></span>
<span data-ttu-id="bd39a-176">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="bd39a-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="bd39a-177">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd39a-177">-Confirm</span></span>
<span data-ttu-id="bd39a-178">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd39a-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd39a-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd39a-179">-WhatIf</span></span>
<span data-ttu-id="bd39a-180">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd39a-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd39a-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd39a-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd39a-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd39a-182">CommonParameters</span></span>
<span data-ttu-id="bd39a-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd39a-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd39a-184">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd39a-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd39a-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd39a-185">INPUTS</span></span>

### <span data-ttu-id="bd39a-186">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bd39a-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bd39a-187">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="bd39a-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="bd39a-188">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bd39a-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bd39a-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd39a-189">OUTPUTS</span></span>

### <span data-ttu-id="bd39a-190">System. void</span><span class="sxs-lookup"><span data-stu-id="bd39a-190">System.Void</span></span>

## <span data-ttu-id="bd39a-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd39a-191">NOTES</span></span>

## <span data-ttu-id="bd39a-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd39a-192">RELATED LINKS</span></span>

[<span data-ttu-id="bd39a-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bd39a-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="bd39a-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bd39a-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="bd39a-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bd39a-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="bd39a-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="bd39a-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="bd39a-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="bd39a-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="bd39a-198">Parar-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bd39a-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
