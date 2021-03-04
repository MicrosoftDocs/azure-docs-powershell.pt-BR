---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 33fcfabb50b0b4af73fe7111c587ac88e746598e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889075"
---
# <span data-ttu-id="577d8-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="577d8-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="577d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577d8-102">SYNOPSIS</span></span>
<span data-ttu-id="577d8-103">Baixa o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="577d8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="577d8-104">SYNTAX</span></span>

### <span data-ttu-id="577d8-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="577d8-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="577d8-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="577d8-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="577d8-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="577d8-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="577d8-108">Arquivo</span><span class="sxs-lookup"><span data-stu-id="577d8-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="577d8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="577d8-109">DESCRIPTION</span></span>
<span data-ttu-id="577d8-110">O cmdlet **Get-AzStorageFileContent** baixa o conteúdo de um arquivo e salva-o em um destino especificado.</span><span class="sxs-lookup"><span data-stu-id="577d8-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="577d8-111">Este cmdlet não retorna o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="577d8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="577d8-112">EXAMPLES</span></span>

### <span data-ttu-id="577d8-113">Exemplo 1: Baixar um arquivo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="577d8-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="577d8-114">Este comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="577d8-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="577d8-115">Exemplo 2: Baixa os arquivos em exemplo de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="577d8-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="577d8-116">Este exemplo baixa os arquivos em exemplo de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="577d8-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="577d8-117">Exemplo 3: baixe um arquivo do Azure em um arquivo local e mantenha as propriedades do SMB de Arquivo do Azure (Atributtes de Arquivo, Hora da Criação de Arquivo, Última Hora de Gravação de Arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="577d8-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="577d8-118">Este exemplo baixa um arquivo do Azure para um arquivo local e preserva as propriedades do SMB do Arquivo do Azure (Atributtes de Arquivo, Hora da Criação de Arquivo, Última Hora de Gravação de Arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="577d8-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="577d8-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="577d8-119">PARAMETERS</span></span>

### <span data-ttu-id="577d8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="577d8-120">-AsJob</span></span>
<span data-ttu-id="577d8-121">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="577d8-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="577d8-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="577d8-122">-CheckMd5</span></span>
<span data-ttu-id="577d8-123">Especifica se a soma Md5 deve ser consultada para o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="577d8-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="577d8-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="577d8-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="577d8-125">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="577d8-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="577d8-126">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="577d8-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="577d8-127">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="577d8-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="577d8-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="577d8-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="577d8-129">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="577d8-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="577d8-130">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="577d8-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="577d8-131">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="577d8-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="577d8-132">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="577d8-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="577d8-133">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="577d8-133">The default value is 10.</span></span>

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

### <span data-ttu-id="577d8-134">-Context</span><span class="sxs-lookup"><span data-stu-id="577d8-134">-Context</span></span>
<span data-ttu-id="577d8-135">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="577d8-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="577d8-136">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577d8-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577d8-137">-DefaultProfile</span></span>
<span data-ttu-id="577d8-138">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="577d8-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577d8-139">-Destination</span><span class="sxs-lookup"><span data-stu-id="577d8-139">-Destination</span></span>
<span data-ttu-id="577d8-140">Especifica o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="577d8-140">Specifies the destination path.</span></span>
<span data-ttu-id="577d8-141">Este cmdlet baixa o conteúdo do arquivo para o local especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="577d8-142">Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="577d8-143">Se você especificar um caminho de um arquivo que já existe e especificar o parâmetro *Force,* o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="577d8-144">Se você especificar um caminho de um arquivo existente e não especificar *Force,* o cmdlet solicitará antes que ele continue.</span><span class="sxs-lookup"><span data-stu-id="577d8-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="577d8-145">Se você especificar o caminho de uma pasta, este cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="577d8-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="577d8-146">-Directory</span></span>
<span data-ttu-id="577d8-147">Especifica uma pasta como um **objeto CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="577d8-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="577d8-148">Este cmdlet obtém conteúdo para um arquivo na pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="577d8-149">Para obter um diretório, use o New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577d8-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="577d8-150">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="577d8-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-151">-File</span><span class="sxs-lookup"><span data-stu-id="577d8-151">-File</span></span>
<span data-ttu-id="577d8-152">Especifica um arquivo como um **objeto CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="577d8-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="577d8-153">Este cmdlet obtém o arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="577d8-154">Para obter um **objeto CloudFile,** use Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577d8-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-155">-Force</span><span class="sxs-lookup"><span data-stu-id="577d8-155">-Force</span></span>
<span data-ttu-id="577d8-156">Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="577d8-157">Se você especificar um caminho de um arquivo que já existe e especificar o parâmetro *Force,* o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="577d8-158">Se você especificar um caminho de um arquivo existente e não especificar *Force,* o cmdlet solicitará antes que ele continue.</span><span class="sxs-lookup"><span data-stu-id="577d8-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="577d8-159">Se você especificar o caminho de uma pasta, este cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="577d8-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="577d8-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="577d8-160">-PassThru</span></span>
<span data-ttu-id="577d8-161">Indica que esse cmdlet retorna o **objeto AzureStorageFile** que ele baixa.</span><span class="sxs-lookup"><span data-stu-id="577d8-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="577d8-162">-Path</span><span class="sxs-lookup"><span data-stu-id="577d8-162">-Path</span></span>
<span data-ttu-id="577d8-163">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="577d8-163">Specifies the path of a file.</span></span>
<span data-ttu-id="577d8-164">Este cmdlet obtém o conteúdo do arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="577d8-165">Se o arquivo não existir, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="577d8-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="577d8-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="577d8-167">Mantenha as propriedades SMB de arquivo de origem (Atribuições de Arquivo, Hora da Criação de Arquivo, Hora da Última Gravação do Arquivo) no Arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="577d8-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="577d8-168">Esse parâmetro só está disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="577d8-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="577d8-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="577d8-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="577d8-170">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="577d8-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="577d8-171">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="577d8-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="577d8-172">-Share</span><span class="sxs-lookup"><span data-stu-id="577d8-172">-Share</span></span>
<span data-ttu-id="577d8-173">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="577d8-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="577d8-174">Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="577d8-175">Para obter um **objeto CloudFileShare,** use Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577d8-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="577d8-176">Este objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="577d8-176">This object contains the storage context.</span></span>
<span data-ttu-id="577d8-177">Se você especificar esse parâmetro, não especifique o *parâmetro Context.*</span><span class="sxs-lookup"><span data-stu-id="577d8-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="577d8-178">-ShareName</span></span>
<span data-ttu-id="577d8-179">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="577d8-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="577d8-180">Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="577d8-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d8-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577d8-181">-Confirm</span></span>
<span data-ttu-id="577d8-182">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577d8-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577d8-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577d8-183">-WhatIf</span></span>
<span data-ttu-id="577d8-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="577d8-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577d8-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="577d8-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577d8-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577d8-186">CommonParameters</span></span>
<span data-ttu-id="577d8-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577d8-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577d8-188">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577d8-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577d8-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="577d8-189">INPUTS</span></span>

### <span data-ttu-id="577d8-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="577d8-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="577d8-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="577d8-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="577d8-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="577d8-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="577d8-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="577d8-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="577d8-194">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="577d8-194">OUTPUTS</span></span>

### <span data-ttu-id="577d8-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="577d8-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="577d8-196">NOTES</span><span class="sxs-lookup"><span data-stu-id="577d8-196">NOTES</span></span>

## <span data-ttu-id="577d8-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="577d8-197">RELATED LINKS</span></span>

[<span data-ttu-id="577d8-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="577d8-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="577d8-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="577d8-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


