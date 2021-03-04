---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 71985cc978425c343e535e6455172f61e5397934
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890060"
---
# <span data-ttu-id="6e618-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6e618-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="6e618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e618-102">SYNOPSIS</span></span>
<span data-ttu-id="6e618-103">Fecha alças de arquivo de um compartilhamento de arquivos, um diretório de arquivos ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e618-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="6e618-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e618-104">SYNTAX</span></span>

### <span data-ttu-id="6e618-105">ShareNameCloseAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e618-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e618-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="6e618-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e618-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="6e618-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e618-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="6e618-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e618-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="6e618-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e618-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="6e618-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e618-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e618-111">DESCRIPTION</span></span>
<span data-ttu-id="6e618-112">O cmdlet **Close-AzStorageFileHandle** fecha as alças de arquivo de um compartilhamento de arquivos ou de um diretório de arquivos ou de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e618-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="6e618-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e618-113">EXAMPLES</span></span>

### <span data-ttu-id="6e618-114">Exemplo 1: lista todos os compartilhamentos de arquivos da Conta de Armazenamento atual e fecha todas as alças de arquivo dos compartilhamentos de arquivos recursivamente.</span><span class="sxs-lookup"><span data-stu-id="6e618-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="6e618-115">Este comando lista todos os compartilhamentos de arquivos da Conta de Armazenamento atual e fecha todas as alças de arquivo dos compartilhamentos de arquivos recursivamente..</span><span class="sxs-lookup"><span data-stu-id="6e618-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="6e618-116">Exemplo 2: Feche todas as alças de arquivo em um diretório de arquivos recursivamente e mostre a contagem de alças de arquivo fechado</span><span class="sxs-lookup"><span data-stu-id="6e618-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="6e618-117">Este comando fecha todas as alças de arquivo em um diretório de arquivos e mostra a contagem de alças de arquivo fechado.</span><span class="sxs-lookup"><span data-stu-id="6e618-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="6e618-118">Exemplo 3: Feche todas as alças de arquivo abertas há 1 dia em um diretório de arquivos</span><span class="sxs-lookup"><span data-stu-id="6e618-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="6e618-119">Este comando lista todas as alças de arquivo em um diretório de arquivos recursivamente, filtra as alças abertas há 1 dia e, em seguida, as fecha.</span><span class="sxs-lookup"><span data-stu-id="6e618-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="6e618-120">Exemplo 4: Fechar todas as alças de arquivo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="6e618-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="6e618-121">Este comando fecha todas as alças de arquivo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e618-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="6e618-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e618-122">PARAMETERS</span></span>

### <span data-ttu-id="6e618-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e618-123">-AsJob</span></span>
<span data-ttu-id="6e618-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6e618-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e618-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e618-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e618-126">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="6e618-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="6e618-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="6e618-127">-CloseAll</span></span>
<span data-ttu-id="6e618-128">Force fechar todas as alças de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e618-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="6e618-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e618-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e618-130">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="6e618-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="6e618-131">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="6e618-131">The default value is 10.</span></span>

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

### <span data-ttu-id="6e618-132">-Context</span><span class="sxs-lookup"><span data-stu-id="6e618-132">-Context</span></span>
<span data-ttu-id="6e618-133">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="6e618-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="6e618-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e618-134">-DefaultProfile</span></span>
<span data-ttu-id="6e618-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e618-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e618-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="6e618-136">-Directory</span></span>
<span data-ttu-id="6e618-137">O objeto CloudFileDirectory indicava a pasta base onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="6e618-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e618-138">-File</span><span class="sxs-lookup"><span data-stu-id="6e618-138">-File</span></span>
<span data-ttu-id="6e618-139">O objeto CloudFile indicava o arquivo para fechar o identificador.</span><span class="sxs-lookup"><span data-stu-id="6e618-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e618-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="6e618-140">-FileHandle</span></span>
<span data-ttu-id="6e618-141">O Alça de Arquivo a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="6e618-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="6e618-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e618-142">-PassThru</span></span>
<span data-ttu-id="6e618-143">Retornar a contagem de alças de arquivo fechado.</span><span class="sxs-lookup"><span data-stu-id="6e618-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="6e618-144">-Path</span><span class="sxs-lookup"><span data-stu-id="6e618-144">-Path</span></span>
<span data-ttu-id="6e618-145">Caminho para um arquivo/diretório existente.</span><span class="sxs-lookup"><span data-stu-id="6e618-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="6e618-146">-Recursivo</span><span class="sxs-lookup"><span data-stu-id="6e618-146">-Recursive</span></span>
<span data-ttu-id="6e618-147">Lista lida com recursivamente.</span><span class="sxs-lookup"><span data-stu-id="6e618-147">List handles Recursively.</span></span>
<span data-ttu-id="6e618-148">Só funciona no Diretório de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="6e618-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="6e618-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e618-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e618-150">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="6e618-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="6e618-151">-Share</span><span class="sxs-lookup"><span data-stu-id="6e618-151">-Share</span></span>
<span data-ttu-id="6e618-152">O objeto CloudFileShare indicava o compartilhamento em que os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="6e618-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e618-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6e618-153">-ShareName</span></span>
<span data-ttu-id="6e618-154">Nome do compartilhamento de arquivos onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="6e618-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="6e618-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e618-155">-Confirm</span></span>
<span data-ttu-id="6e618-156">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e618-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e618-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e618-157">-WhatIf</span></span>
<span data-ttu-id="6e618-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e618-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e618-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e618-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e618-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e618-160">CommonParameters</span></span>
<span data-ttu-id="6e618-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e618-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e618-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e618-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e618-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e618-163">INPUTS</span></span>

### <span data-ttu-id="6e618-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6e618-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="6e618-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="6e618-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="6e618-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e618-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e618-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e618-167">OUTPUTS</span></span>

### <span data-ttu-id="6e618-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="6e618-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="6e618-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e618-169">NOTES</span></span>

## <span data-ttu-id="6e618-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e618-170">RELATED LINKS</span></span>
