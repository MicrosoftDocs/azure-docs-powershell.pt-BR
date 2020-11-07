---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 756819d39764fc0d12cd08e0bf0d3edd447cca51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774130"
---
# <span data-ttu-id="2167a-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2167a-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="2167a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2167a-102">SYNOPSIS</span></span>
<span data-ttu-id="2167a-103">Baixa o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="2167a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2167a-104">SYNTAX</span></span>

### <span data-ttu-id="2167a-105">Nome_do_compartilhamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="2167a-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2167a-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="2167a-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2167a-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="2167a-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2167a-108">Arquivos</span><span class="sxs-lookup"><span data-stu-id="2167a-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="2167a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2167a-109">DESCRIPTION</span></span>
<span data-ttu-id="2167a-110">O cmdlet **Get-AzStorageFileContent** faz o download do conteúdo de um arquivo e, em seguida, o salva em um destino que você especificar.</span><span class="sxs-lookup"><span data-stu-id="2167a-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="2167a-111">Esse cmdlet não retorna o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="2167a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2167a-112">EXAMPLES</span></span>

### <span data-ttu-id="2167a-113">Exemplo 1: baixar um arquivo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="2167a-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="2167a-114">Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="2167a-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="2167a-115">Exemplo 2: baixar os arquivos em compartilhamento de arquivo de exemplo</span><span class="sxs-lookup"><span data-stu-id="2167a-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="2167a-116">Este exemplo baixa os arquivos em um exemplo de compartilhamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="2167a-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="2167a-117">Exemplo 3: baixar um arquivo do Azure para um arquivo local e perservindo as propriedades do Azure File SMB (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2167a-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="2167a-118">Este exemplo baixa um arquivo do Azure para um arquivo local e perpreserve as propriedades do Azure File SMB (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2167a-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="2167a-119">OS</span><span class="sxs-lookup"><span data-stu-id="2167a-119">PARAMETERS</span></span>

### <span data-ttu-id="2167a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2167a-120">-AsJob</span></span>
<span data-ttu-id="2167a-121">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2167a-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2167a-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2167a-122">-CheckMd5</span></span>
<span data-ttu-id="2167a-123">Especifica se a soma MD5 deve ser verificada pelo arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="2167a-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="2167a-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2167a-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2167a-125">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="2167a-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="2167a-126">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2167a-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="2167a-127">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2167a-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2167a-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2167a-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2167a-129">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2167a-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="2167a-130">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2167a-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="2167a-131">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="2167a-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="2167a-132">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2167a-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="2167a-133">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="2167a-133">The default value is 10.</span></span>

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

### <span data-ttu-id="2167a-134">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2167a-134">-Context</span></span>
<span data-ttu-id="2167a-135">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2167a-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="2167a-136">Para obter um contexto, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2167a-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2167a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2167a-137">-DefaultProfile</span></span>
<span data-ttu-id="2167a-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2167a-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2167a-139">-Destino</span><span class="sxs-lookup"><span data-stu-id="2167a-139">-Destination</span></span>
<span data-ttu-id="2167a-140">Especifica o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="2167a-140">Specifies the destination path.</span></span>
<span data-ttu-id="2167a-141">Esse cmdlet baixa o conteúdo do arquivo para o local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="2167a-142">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2167a-143">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2167a-144">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="2167a-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="2167a-145">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2167a-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2167a-146">-Diretório</span><span class="sxs-lookup"><span data-stu-id="2167a-146">-Directory</span></span>
<span data-ttu-id="2167a-147">Especifica uma pasta como um objeto **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="2167a-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2167a-148">Esse cmdlet obtém conteúdo para um arquivo na pasta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="2167a-149">Para obter um diretório, use o cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2167a-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2167a-150">Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.</span><span class="sxs-lookup"><span data-stu-id="2167a-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2167a-151">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="2167a-151">-File</span></span>
<span data-ttu-id="2167a-152">Especifica um arquivo como um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="2167a-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="2167a-153">Esse cmdlet obtém o arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="2167a-154">Para obter um objeto **cloudfile** , use o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="2167a-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2167a-155">-Force</span><span class="sxs-lookup"><span data-stu-id="2167a-155">-Force</span></span>
<span data-ttu-id="2167a-156">Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2167a-157">Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2167a-158">Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="2167a-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="2167a-159">Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2167a-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2167a-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2167a-160">-PassThru</span></span>
<span data-ttu-id="2167a-161">Indica que esse cmdlet retorna o objeto **AzureStorageFile** que ele baixa.</span><span class="sxs-lookup"><span data-stu-id="2167a-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="2167a-162">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2167a-162">-Path</span></span>
<span data-ttu-id="2167a-163">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2167a-163">Specifies the path of a file.</span></span>
<span data-ttu-id="2167a-164">Esse cmdlet obtém o conteúdo do arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="2167a-165">Se o arquivo não existir, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2167a-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2167a-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="2167a-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="2167a-167">Mantenha as propriedades SMB do arquivo de origem (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2167a-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="2167a-168">Este parâmetro só está disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="2167a-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="2167a-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2167a-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2167a-170">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="2167a-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="2167a-171">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="2167a-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2167a-172">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="2167a-172">-Share</span></span>
<span data-ttu-id="2167a-173">Especifica um objeto **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="2167a-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2167a-174">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="2167a-175">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2167a-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="2167a-176">Esse objeto contém o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2167a-176">This object contains the storage context.</span></span>
<span data-ttu-id="2167a-177">Se você especificar esse parâmetro, não especifique o parâmetro *Context* .</span><span class="sxs-lookup"><span data-stu-id="2167a-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2167a-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2167a-178">-ShareName</span></span>
<span data-ttu-id="2167a-179">Especifica o nome do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2167a-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="2167a-180">Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2167a-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="2167a-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2167a-181">-Confirm</span></span>
<span data-ttu-id="2167a-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2167a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2167a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2167a-183">-WhatIf</span></span>
<span data-ttu-id="2167a-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2167a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2167a-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2167a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2167a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2167a-186">CommonParameters</span></span>
<span data-ttu-id="2167a-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2167a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2167a-188">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2167a-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2167a-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2167a-189">INPUTS</span></span>

### <span data-ttu-id="2167a-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2167a-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2167a-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2167a-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="2167a-192">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="2167a-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="2167a-193">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2167a-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2167a-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2167a-194">OUTPUTS</span></span>

### <span data-ttu-id="2167a-195">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="2167a-195">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="2167a-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2167a-196">NOTES</span></span>

## <span data-ttu-id="2167a-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2167a-197">RELATED LINKS</span></span>

[<span data-ttu-id="2167a-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="2167a-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="2167a-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2167a-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)

