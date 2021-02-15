---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112502"
---
# <span data-ttu-id="c1a07-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1a07-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="c1a07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1a07-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a07-103">Começa a copiar um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="c1a07-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1a07-104">SYNTAX</span></span>

### <span data-ttu-id="c1a07-105">Containername</span><span class="sxs-lookup"><span data-stu-id="c1a07-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1a07-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1a07-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="c1a07-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="c1a07-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-109">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c1a07-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1a07-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="c1a07-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="c1a07-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="c1a07-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="c1a07-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a07-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="c1a07-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a07-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1a07-115">DESCRIPTION</span></span>
<span data-ttu-id="c1a07-116">O cmdlet **Start-AzStorageFileCopy** começa a copiar um arquivo de origem para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1a07-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="c1a07-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1a07-117">EXAMPLES</span></span>

### <span data-ttu-id="c1a07-118">Exemplo 1: Iniciar a operação de cópia de arquivo para arquivo usando o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="c1a07-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="c1a07-119">Esse comando inicia uma operação de cópia de arquivo para arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1a07-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="c1a07-120">O comando especifica o nome do compartilhamento e o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="c1a07-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="c1a07-121">Exemplo 2: Iniciar a operação de cópia de blob para arquivo usando o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="c1a07-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="c1a07-122">Esse comando inicia uma operação de cópia de blob para arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1a07-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="c1a07-123">O comando especifica o nome do contêiner e o nome do blob</span><span class="sxs-lookup"><span data-stu-id="c1a07-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="c1a07-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1a07-124">PARAMETERS</span></span>

### <span data-ttu-id="c1a07-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="c1a07-125">-AbsoluteUri</span></span>
<span data-ttu-id="c1a07-126">Especifica o URI do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="c1a07-127">Se o local de origem exigir uma credencial, você deverá fornecer uma.</span><span class="sxs-lookup"><span data-stu-id="c1a07-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="c1a07-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1a07-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c1a07-129">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c1a07-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c1a07-130">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c1a07-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c1a07-131">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c1a07-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c1a07-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c1a07-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c1a07-133">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c1a07-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c1a07-134">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c1a07-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c1a07-135">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c1a07-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c1a07-136">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c1a07-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c1a07-137">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c1a07-137">The default value is 10.</span></span>

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

### <span data-ttu-id="c1a07-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c1a07-138">-Context</span></span>
<span data-ttu-id="c1a07-139">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a07-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c1a07-140">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a07-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a07-141">-DefaultProfile</span></span>
<span data-ttu-id="c1a07-142">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a07-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a07-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="c1a07-143">-DestContext</span></span>
<span data-ttu-id="c1a07-144">Especifica o contexto de Armazenamento do Azure do destino.</span><span class="sxs-lookup"><span data-stu-id="c1a07-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="c1a07-145">Para obter um contexto, use **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="c1a07-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="c1a07-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="c1a07-146">-DestFile</span></span>
<span data-ttu-id="c1a07-147">Especifica um objeto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="c1a07-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c1a07-148">Você pode criar um arquivo na nuvem ou obter um usando o cmdlet Get-AzStorageFile nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="c1a07-149">-DestFilePath</span></span>
<span data-ttu-id="c1a07-150">Especifica o caminho do arquivo de destino em relação ao compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="c1a07-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="c1a07-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="c1a07-151">-DestShareName</span></span>
<span data-ttu-id="c1a07-152">Especifica o nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="c1a07-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="c1a07-153">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c1a07-153">-Force</span></span>
<span data-ttu-id="c1a07-154">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1a07-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1a07-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1a07-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c1a07-156">Especifica a duração do período de tempo de tempo para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c1a07-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c1a07-157">-SrcB cdc</span><span class="sxs-lookup"><span data-stu-id="c1a07-157">-SrcBlob</span></span>
<span data-ttu-id="c1a07-158">Especifica um objeto **CloudB ltd.**</span><span class="sxs-lookup"><span data-stu-id="c1a07-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="c1a07-159">Você pode criar um blob de nuvem ou obter um usando o cmdlet Get-AzStorageBlob nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-160">-SrcBname</span><span class="sxs-lookup"><span data-stu-id="c1a07-160">-SrcBlobName</span></span>
<span data-ttu-id="c1a07-161">Especifica o nome do blob de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="c1a07-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="c1a07-162">-SrcContainer</span></span>
<span data-ttu-id="c1a07-163">Especifica um objeto de contêiner de blob na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="c1a07-164">Você pode criar objeto de contêiner de blob na nuvem ou usar o cmdlet Get-AzStorageContainer nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="c1a07-165">-SrcContainerName</span></span>
<span data-ttu-id="c1a07-166">Especifica o nome do contêiner de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="c1a07-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="c1a07-167">-SrcFile</span></span>
<span data-ttu-id="c1a07-168">Especifica um objeto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="c1a07-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c1a07-169">Você pode criar um arquivo na nuvem ou obter um usando **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="c1a07-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="c1a07-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="c1a07-170">-SrcFilePath</span></span>
<span data-ttu-id="c1a07-171">Especifica o caminho do arquivo de origem em relação ao diretório de origem ou ao compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="c1a07-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="c1a07-172">-SrcShare</span></span>
<span data-ttu-id="c1a07-173">Especifica um objeto de compartilhamento de arquivo na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="c1a07-174">Você pode criar um compartilhamento de arquivos na nuvem ou obter um usando o cmdlet Get-AzStorageShare nuvem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="c1a07-175">-SrcShareName</span></span>
<span data-ttu-id="c1a07-176">Especifica o nome do compartilhamento de origem.</span><span class="sxs-lookup"><span data-stu-id="c1a07-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="c1a07-177">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1a07-177">-Confirm</span></span>
<span data-ttu-id="c1a07-178">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a07-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a07-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a07-179">-WhatIf</span></span>
<span data-ttu-id="c1a07-180">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1a07-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a07-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1a07-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a07-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a07-182">CommonParameters</span></span>
<span data-ttu-id="c1a07-183">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a07-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a07-184">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a07-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a07-185">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1a07-185">INPUTS</span></span>

### <span data-ttu-id="c1a07-186">Microsoft.Azure.Storage.Blob.CloudBlab</span><span class="sxs-lookup"><span data-stu-id="c1a07-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c1a07-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="c1a07-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="c1a07-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1a07-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1a07-189">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1a07-189">OUTPUTS</span></span>

### <span data-ttu-id="c1a07-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c1a07-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="c1a07-191">Notas</span><span class="sxs-lookup"><span data-stu-id="c1a07-191">NOTES</span></span>

## <span data-ttu-id="c1a07-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1a07-192">RELATED LINKS</span></span>

[<span data-ttu-id="c1a07-193">Get-AzStorageB ltd</span><span class="sxs-lookup"><span data-stu-id="c1a07-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c1a07-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1a07-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="c1a07-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="c1a07-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="c1a07-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1a07-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c1a07-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c1a07-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="c1a07-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1a07-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
