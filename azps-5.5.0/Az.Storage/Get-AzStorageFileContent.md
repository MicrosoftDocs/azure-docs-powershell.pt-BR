---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110881"
---
# <span data-ttu-id="a6bf0-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6bf0-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="a6bf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bf0-103">Baixa o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="a6bf0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6bf0-104">SYNTAX</span></span>

### <span data-ttu-id="a6bf0-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6bf0-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="a6bf0-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a6bf0-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="a6bf0-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="a6bf0-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="a6bf0-108">Arquivo</span><span class="sxs-lookup"><span data-stu-id="a6bf0-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="a6bf0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6bf0-109">DESCRIPTION</span></span>
<span data-ttu-id="a6bf0-110">O cmdlet **Get-AzStorageFileContent** baixa o conteúdo de um arquivo e o salva em um destino especificado por você.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="a6bf0-111">Este cmdlet não retorna o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="a6bf0-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6bf0-112">EXAMPLES</span></span>

### <span data-ttu-id="a6bf0-113">Exemplo 1: Baixar um arquivo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="a6bf0-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="a6bf0-114">Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="a6bf0-115">Exemplo 2: baixa os arquivos em exemplo de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a6bf0-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="a6bf0-116">Este exemplo baixa os arquivos em exemplo de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a6bf0-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="a6bf0-117">Exemplo 3: baixe um arquivo do Azure para um arquivo local e mantenha as propriedades SMB do Arquivo do Azure (Arquivo Atribuído, Hora de Criação de Arquivo, Hora da Última Gravação do Arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="a6bf0-118">Este exemplo baixa um arquivo do Azure para um arquivo local e conserva as propriedades SMB do Arquivo do Azure (Azure File Attributtes, Tempo de Criação de Arquivo, Hora da Última Gravação do Arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="a6bf0-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6bf0-119">PARAMETERS</span></span>

### <span data-ttu-id="a6bf0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6bf0-120">-AsJob</span></span>
<span data-ttu-id="a6bf0-121">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a6bf0-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="a6bf0-122">-CheckMd5</span></span>
<span data-ttu-id="a6bf0-123">Especifica se você deve verificar a soma Md5 do arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="a6bf0-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6bf0-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6bf0-125">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="a6bf0-126">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="a6bf0-127">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6bf0-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6bf0-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6bf0-129">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="a6bf0-130">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="a6bf0-131">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="a6bf0-132">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="a6bf0-133">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-133">The default value is 10.</span></span>

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

### <span data-ttu-id="a6bf0-134">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a6bf0-134">-Context</span></span>
<span data-ttu-id="a6bf0-135">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="a6bf0-136">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a6bf0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bf0-137">-DefaultProfile</span></span>
<span data-ttu-id="a6bf0-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bf0-139">-Destino</span><span class="sxs-lookup"><span data-stu-id="a6bf0-139">-Destination</span></span>
<span data-ttu-id="a6bf0-140">Especifica o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-140">Specifies the destination path.</span></span>
<span data-ttu-id="a6bf0-141">Este cmdlet baixa o conteúdo do arquivo para o local especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="a6bf0-142">Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="a6bf0-143">Se você especificar um caminho de um arquivo  que já existe e especificar o parâmetro Force, o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="a6bf0-144">Se você especificar um caminho de um arquivo existente e não especificar *Forçar,* o cmdlet solicitará antes que ele continue.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="a6bf0-145">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="a6bf0-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="a6bf0-146">-Directory</span></span>
<span data-ttu-id="a6bf0-147">Especifica uma pasta como um objeto **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="a6bf0-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a6bf0-148">Este cmdlet obtém conteúdo para um arquivo na pasta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="a6bf0-149">Para obter um diretório, use o New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="a6bf0-150">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="a6bf0-151">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="a6bf0-151">-File</span></span>
<span data-ttu-id="a6bf0-152">Especifica um arquivo como um objeto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="a6bf0-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="a6bf0-153">Este cmdlet obtém o arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="a6bf0-154">Para obter um **objeto CloudFile,** use o cmdlet Get-AzStorageFile nuvem.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="a6bf0-155">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a6bf0-155">-Force</span></span>
<span data-ttu-id="a6bf0-156">Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="a6bf0-157">Se você especificar um caminho de um arquivo  que já existe e especificar o parâmetro Force, o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="a6bf0-158">Se você especificar um caminho de um arquivo existente e não especificar *Forçar,* o cmdlet solicitará antes que ele continue.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="a6bf0-159">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="a6bf0-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bf0-160">-PassThru</span></span>
<span data-ttu-id="a6bf0-161">Indica que esse cmdlet retorna o objeto **AzureStorageFile** baixado.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="a6bf0-162">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a6bf0-162">-Path</span></span>
<span data-ttu-id="a6bf0-163">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-163">Specifies the path of a file.</span></span>
<span data-ttu-id="a6bf0-164">Este cmdlet obtém o conteúdo do arquivo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="a6bf0-165">Se o arquivo não existir, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6bf0-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="a6bf0-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="a6bf0-167">Mantenha as propriedades SMB de arquivo de origem (Arquivo autribuções, Hora de Criação de Arquivo, Hora da Última Gravação do Arquivo) no Arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="a6bf0-168">Este parâmetro só está disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="a6bf0-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6bf0-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6bf0-170">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="a6bf0-171">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a6bf0-172">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a6bf0-172">-Share</span></span>
<span data-ttu-id="a6bf0-173">Especifica um **objeto CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="a6bf0-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a6bf0-174">Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="a6bf0-175">Para obter um **objeto CloudFileShare,** use o cmdlet Get-AzStorageShare nuvem.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="a6bf0-176">Este objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-176">This object contains the storage context.</span></span>
<span data-ttu-id="a6bf0-177">Se você especificar esse parâmetro, não especifique o *parâmetro De* contexto.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a6bf0-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a6bf0-178">-ShareName</span></span>
<span data-ttu-id="a6bf0-179">Especifica o nome do compartilhamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="a6bf0-180">Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="a6bf0-181">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a6bf0-181">-Confirm</span></span>
<span data-ttu-id="a6bf0-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bf0-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bf0-183">-WhatIf</span></span>
<span data-ttu-id="a6bf0-184">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bf0-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bf0-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bf0-186">CommonParameters</span></span>
<span data-ttu-id="a6bf0-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bf0-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bf0-188">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6bf0-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bf0-189">Entradas</span><span class="sxs-lookup"><span data-stu-id="a6bf0-189">INPUTS</span></span>

### <span data-ttu-id="a6bf0-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a6bf0-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a6bf0-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a6bf0-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a6bf0-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="a6bf0-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="a6bf0-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6bf0-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6bf0-194">Saídas</span><span class="sxs-lookup"><span data-stu-id="a6bf0-194">OUTPUTS</span></span>

### <span data-ttu-id="a6bf0-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="a6bf0-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="a6bf0-196">Notas</span><span class="sxs-lookup"><span data-stu-id="a6bf0-196">NOTES</span></span>

## <span data-ttu-id="a6bf0-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6bf0-197">RELATED LINKS</span></span>

[<span data-ttu-id="a6bf0-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="a6bf0-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="a6bf0-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a6bf0-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


