---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: cca517246f548deb64cba1b4bc737de88628e7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774024"
---
# <span data-ttu-id="9075d-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="9075d-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="9075d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9075d-102">SYNOPSIS</span></span>
<span data-ttu-id="9075d-103">Fecha identificadores de arquivos de um compartilhamento de arquivos, um diretório de arquivos ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9075d-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="9075d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9075d-104">SYNTAX</span></span>

### <span data-ttu-id="9075d-105">ShareNameCloseAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="9075d-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9075d-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="9075d-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9075d-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="9075d-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9075d-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="9075d-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9075d-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="9075d-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9075d-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="9075d-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9075d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9075d-111">DESCRIPTION</span></span>
<span data-ttu-id="9075d-112">O cmdlet **Close-AzStorageFileHandle** fecha identificadores de arquivo de um compartilhamento de arquivos ou diretório de arquivos ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9075d-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="9075d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9075d-113">EXAMPLES</span></span>

### <span data-ttu-id="9075d-114">Exemplo 1: lista todos os compartilhamentos de arquivos da conta de armazenamento atual e fecha todos os identificadores de arquivo do compartilhamento de arquivos recursivamente.</span><span class="sxs-lookup"><span data-stu-id="9075d-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="9075d-115">Esse comando lista todos os compartilhamentos de arquivos da conta de armazenamento atual e fecha todos os identificadores de arquivo dos compartilhamentos de arquivos recursivamente..</span><span class="sxs-lookup"><span data-stu-id="9075d-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="9075d-116">Exemplo 2: fechar todos os identificadores de arquivo em um diretório de arquivos recursivamente e mostrar a contagem de identificadores de arquivos fechados</span><span class="sxs-lookup"><span data-stu-id="9075d-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="9075d-117">Esse comando fecha todos os identificadores de arquivo em um diretório de arquivos e mostra a contagem de identificadores de arquivos fechados.</span><span class="sxs-lookup"><span data-stu-id="9075d-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="9075d-118">Exemplo 3: fechar todos os identificadores de arquivo abertos há 1 dia atrás em um diretório de arquivos</span><span class="sxs-lookup"><span data-stu-id="9075d-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="9075d-119">Esse comando lista todos os identificadores de arquivos em um diretório de arquivos recursivamente, filtra as alças abertas há um dia e, em seguida, feche-os.</span><span class="sxs-lookup"><span data-stu-id="9075d-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="9075d-120">Exemplo 4: fechar todos os identificadores de arquivo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="9075d-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="9075d-121">Esse comando fecha todos os identificadores de arquivo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9075d-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="9075d-122">OS</span><span class="sxs-lookup"><span data-stu-id="9075d-122">PARAMETERS</span></span>

### <span data-ttu-id="9075d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9075d-123">-AsJob</span></span>
<span data-ttu-id="9075d-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9075d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9075d-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9075d-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9075d-126">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="9075d-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="9075d-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="9075d-127">-CloseAll</span></span>
<span data-ttu-id="9075d-128">Force fechar todos os identificadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9075d-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9075d-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9075d-130">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9075d-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="9075d-131">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9075d-131">The default value is 10.</span></span>

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

### <span data-ttu-id="9075d-132">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9075d-132">-Context</span></span>
<span data-ttu-id="9075d-133">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9075d-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9075d-134">-DefaultProfile</span></span>
<span data-ttu-id="9075d-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9075d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9075d-136">-Diretório</span><span class="sxs-lookup"><span data-stu-id="9075d-136">-Directory</span></span>
<span data-ttu-id="9075d-137">CloudFileDirectory objeto indicou a pasta base na qual os arquivos/diretórios serão listados.</span><span class="sxs-lookup"><span data-stu-id="9075d-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-138">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="9075d-138">-File</span></span>
<span data-ttu-id="9075d-139">O objeto cloudfile indicou o arquivo para fechar o identificador.</span><span class="sxs-lookup"><span data-stu-id="9075d-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-140">-Identificador de</span><span class="sxs-lookup"><span data-stu-id="9075d-140">-FileHandle</span></span>
<span data-ttu-id="9075d-141">O identificador de arquivo a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="9075d-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9075d-142">-PassThru</span></span>
<span data-ttu-id="9075d-143">Retorne a contagem de identificadores de arquivo fechados.</span><span class="sxs-lookup"><span data-stu-id="9075d-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="9075d-144">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9075d-144">-Path</span></span>
<span data-ttu-id="9075d-145">Caminho para um arquivo/diretório existente.</span><span class="sxs-lookup"><span data-stu-id="9075d-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-146">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="9075d-146">-Recursive</span></span>
<span data-ttu-id="9075d-147">Liste as alças recursivamente.</span><span class="sxs-lookup"><span data-stu-id="9075d-147">List handles Recursively.</span></span>
<span data-ttu-id="9075d-148">Só funciona no diretório de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9075d-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9075d-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9075d-150">O tempo limite do servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="9075d-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="9075d-151">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="9075d-151">-Share</span></span>
<span data-ttu-id="9075d-152">O objeto CloudFileShare indicou o compartilhamento em que os arquivos/diretórios serão listados.</span><span class="sxs-lookup"><span data-stu-id="9075d-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9075d-153">-ShareName</span></span>
<span data-ttu-id="9075d-154">Nome do compartilhamento de arquivos em que os arquivos/diretórios serão listados.</span><span class="sxs-lookup"><span data-stu-id="9075d-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9075d-155">-Confirm</span></span>
<span data-ttu-id="9075d-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9075d-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9075d-157">-WhatIf</span></span>
<span data-ttu-id="9075d-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9075d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9075d-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9075d-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9075d-160">CommonParameters</span></span>
<span data-ttu-id="9075d-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9075d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9075d-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9075d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9075d-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9075d-163">INPUTS</span></span>

### <span data-ttu-id="9075d-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9075d-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9075d-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9075d-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9075d-166">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9075d-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9075d-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9075d-167">OUTPUTS</span></span>

### <span data-ttu-id="9075d-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="9075d-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="9075d-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9075d-169">NOTES</span></span>

## <span data-ttu-id="9075d-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9075d-170">RELATED LINKS</span></span>