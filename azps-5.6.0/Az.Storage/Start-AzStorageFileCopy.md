---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2b3bea343e5d4e2267c2bec14d60564392914a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886395"
---
# <span data-ttu-id="98389-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98389-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="98389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98389-102">SYNOPSIS</span></span>
<span data-ttu-id="98389-103">Começa a copiar um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="98389-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="98389-104">SYNTAX</span></span>

### <span data-ttu-id="98389-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="98389-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98389-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="98389-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="98389-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="98389-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="98389-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98389-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="98389-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="98389-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="98389-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="98389-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98389-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="98389-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98389-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="98389-115">DESCRIPTION</span></span>
<span data-ttu-id="98389-116">O cmdlet **Start-AzStorageFileCopy** começa a copiar um arquivo de origem para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="98389-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="98389-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98389-117">EXAMPLES</span></span>

### <span data-ttu-id="98389-118">Exemplo 1: Iniciar a operação de cópia de arquivo para arquivo usando o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="98389-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="98389-119">Este comando inicia uma operação de cópia de arquivo para arquivo.</span><span class="sxs-lookup"><span data-stu-id="98389-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="98389-120">O comando especifica o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="98389-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="98389-121">Exemplo 2: Iniciar a operação de cópia de blob para arquivo usando o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="98389-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="98389-122">Este comando inicia uma operação de cópia de blob para arquivo.</span><span class="sxs-lookup"><span data-stu-id="98389-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="98389-123">O comando especifica o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="98389-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="98389-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="98389-124">PARAMETERS</span></span>

### <span data-ttu-id="98389-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="98389-125">-AbsoluteUri</span></span>
<span data-ttu-id="98389-126">Especifica o URI do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="98389-127">Se o local de origem exigir uma credencial, você deve fornecer uma.</span><span class="sxs-lookup"><span data-stu-id="98389-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="98389-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98389-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="98389-129">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="98389-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="98389-130">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="98389-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="98389-131">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="98389-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="98389-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="98389-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="98389-133">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="98389-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="98389-134">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="98389-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="98389-135">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="98389-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="98389-136">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="98389-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="98389-137">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="98389-137">The default value is 10.</span></span>

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

### <span data-ttu-id="98389-138">-Context</span><span class="sxs-lookup"><span data-stu-id="98389-138">-Context</span></span>
<span data-ttu-id="98389-139">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="98389-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="98389-140">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98389-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="98389-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98389-141">-DefaultProfile</span></span>
<span data-ttu-id="98389-142">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98389-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98389-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="98389-143">-DestContext</span></span>
<span data-ttu-id="98389-144">Especifica o contexto de Armazenamento do Azure do destino.</span><span class="sxs-lookup"><span data-stu-id="98389-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="98389-145">Para obter um contexto, use **New-AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="98389-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="98389-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="98389-146">-DestFile</span></span>
<span data-ttu-id="98389-147">Especifica um **objeto CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="98389-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="98389-148">Você pode criar um arquivo de nuvem ou obter um usando Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98389-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="98389-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="98389-149">-DestFilePath</span></span>
<span data-ttu-id="98389-150">Especifica o caminho do arquivo de destino em relação ao compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="98389-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="98389-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="98389-151">-DestShareName</span></span>
<span data-ttu-id="98389-152">Especifica o nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="98389-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="98389-153">-Force</span><span class="sxs-lookup"><span data-stu-id="98389-153">-Force</span></span>
<span data-ttu-id="98389-154">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="98389-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98389-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98389-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="98389-156">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="98389-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="98389-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="98389-157">-SrcBlob</span></span>
<span data-ttu-id="98389-158">Especifica um **objeto CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="98389-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="98389-159">Você pode criar um blob de nuvem ou obter um usando o cmdlet Get-AzStorageBlob de nuvem.</span><span class="sxs-lookup"><span data-stu-id="98389-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="98389-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="98389-160">-SrcBlobName</span></span>
<span data-ttu-id="98389-161">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="98389-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="98389-162">-SrcContainer</span></span>
<span data-ttu-id="98389-163">Especifica um objeto contêiner de blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="98389-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="98389-164">Você pode criar um objeto contêiner de blob na nuvem ou usar o cmdlet Get-AzStorageContainer nuvem.</span><span class="sxs-lookup"><span data-stu-id="98389-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="98389-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="98389-165">-SrcContainerName</span></span>
<span data-ttu-id="98389-166">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="98389-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="98389-167">-SrcFile</span></span>
<span data-ttu-id="98389-168">Especifica um **objeto CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="98389-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="98389-169">Você pode criar um arquivo de nuvem ou obter um **usando Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="98389-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98389-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="98389-170">-SrcFilePath</span></span>
<span data-ttu-id="98389-171">Especifica o caminho do arquivo de origem em relação ao diretório de origem ou ao compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="98389-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="98389-172">-SrcShare</span></span>
<span data-ttu-id="98389-173">Especifica um objeto de compartilhamento de arquivos na nuvem.</span><span class="sxs-lookup"><span data-stu-id="98389-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="98389-174">Você pode criar um compartilhamento de arquivos na nuvem ou obter um usando o cmdlet Get-AzStorageShare de nuvem.</span><span class="sxs-lookup"><span data-stu-id="98389-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98389-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="98389-175">-SrcShareName</span></span>
<span data-ttu-id="98389-176">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="98389-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="98389-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98389-177">-Confirm</span></span>
<span data-ttu-id="98389-178">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98389-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98389-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98389-179">-WhatIf</span></span>
<span data-ttu-id="98389-180">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98389-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98389-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98389-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98389-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98389-182">CommonParameters</span></span>
<span data-ttu-id="98389-183">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98389-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98389-184">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98389-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98389-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98389-185">INPUTS</span></span>

### <span data-ttu-id="98389-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="98389-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="98389-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="98389-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="98389-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98389-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98389-189">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="98389-189">OUTPUTS</span></span>

### <span data-ttu-id="98389-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="98389-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="98389-191">NOTES</span><span class="sxs-lookup"><span data-stu-id="98389-191">NOTES</span></span>

## <span data-ttu-id="98389-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98389-192">RELATED LINKS</span></span>

[<span data-ttu-id="98389-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="98389-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="98389-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="98389-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="98389-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="98389-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="98389-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="98389-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="98389-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="98389-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="98389-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98389-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
