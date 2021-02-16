---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113938"
---
# <span data-ttu-id="02bd5-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="02bd5-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="02bd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="02bd5-103">Fecha alças de arquivo de um compartilhamento de arquivos, um diretório de arquivos ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="02bd5-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="02bd5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02bd5-104">SYNTAX</span></span>

### <span data-ttu-id="02bd5-105">ShareNameCloseAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="02bd5-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02bd5-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="02bd5-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02bd5-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="02bd5-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02bd5-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="02bd5-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02bd5-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="02bd5-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02bd5-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="02bd5-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02bd5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="02bd5-111">DESCRIPTION</span></span>
<span data-ttu-id="02bd5-112">O cmdlet **Close-AzStorageFileHandle** fecha as alças de arquivo de um compartilhamento de arquivos, de um diretório de arquivos ou de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="02bd5-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="02bd5-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02bd5-113">EXAMPLES</span></span>

### <span data-ttu-id="02bd5-114">Exemplo 1: Lista todos os compartilhamentos de arquivos da Conta de Armazenamento atual e fecha todas as alças de arquivo dos compartilhamentos de arquivos recursivamente.</span><span class="sxs-lookup"><span data-stu-id="02bd5-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="02bd5-115">Esse comando lista todos os compartilhamentos de arquivos da Conta de Armazenamento atual e fecha todas as alças de arquivo do arquivo compartilha recursivamente..</span><span class="sxs-lookup"><span data-stu-id="02bd5-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="02bd5-116">Exemplo 2: Fechar todas as alças de arquivo em um diretório de arquivos recursivamente e mostrar a contagem de alças de arquivo fechada</span><span class="sxs-lookup"><span data-stu-id="02bd5-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="02bd5-117">Esse comando fecha todas as alças de arquivo em um diretório de arquivos e mostra a contagem de alças de arquivo fechada.</span><span class="sxs-lookup"><span data-stu-id="02bd5-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="02bd5-118">Exemplo 3: Fechar todas as alças de arquivo que foi aberta há um dia em um diretório de arquivos</span><span class="sxs-lookup"><span data-stu-id="02bd5-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="02bd5-119">Esse comando lista todas as alças de arquivo em um diretório de arquivos recursivamente, filtra as alças que foram abertas há um dia e, em seguida, feche-as.</span><span class="sxs-lookup"><span data-stu-id="02bd5-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="02bd5-120">Exemplo 4: Fechar todas as alças de arquivo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="02bd5-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="02bd5-121">Esse comando fecha todas as alças de arquivo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="02bd5-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="02bd5-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02bd5-122">PARAMETERS</span></span>

### <span data-ttu-id="02bd5-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02bd5-123">-AsJob</span></span>
<span data-ttu-id="02bd5-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="02bd5-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02bd5-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02bd5-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02bd5-126">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="02bd5-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="02bd5-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="02bd5-127">-CloseAll</span></span>
<span data-ttu-id="02bd5-128">Forçar o fechamento de todas as alças de arquivo.</span><span class="sxs-lookup"><span data-stu-id="02bd5-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="02bd5-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02bd5-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02bd5-130">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="02bd5-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="02bd5-131">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="02bd5-131">The default value is 10.</span></span>

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

### <span data-ttu-id="02bd5-132">-Contexto</span><span class="sxs-lookup"><span data-stu-id="02bd5-132">-Context</span></span>
<span data-ttu-id="02bd5-133">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="02bd5-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="02bd5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02bd5-134">-DefaultProfile</span></span>
<span data-ttu-id="02bd5-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02bd5-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02bd5-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="02bd5-136">-Directory</span></span>
<span data-ttu-id="02bd5-137">O objeto CloudFileDirectory indicou a pasta base onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="02bd5-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02bd5-138">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="02bd5-138">-File</span></span>
<span data-ttu-id="02bd5-139">O objeto CloudFile indicou a alça de fechamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="02bd5-139">CloudFile object indicated the file to close handle.</span></span>

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

### <span data-ttu-id="02bd5-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="02bd5-140">-FileHandle</span></span>
<span data-ttu-id="02bd5-141">A Alça de Arquivo a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="02bd5-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="02bd5-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02bd5-142">-PassThru</span></span>
<span data-ttu-id="02bd5-143">Retorna a contagem de alças de arquivo fechadas.</span><span class="sxs-lookup"><span data-stu-id="02bd5-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="02bd5-144">-Caminho</span><span class="sxs-lookup"><span data-stu-id="02bd5-144">-Path</span></span>
<span data-ttu-id="02bd5-145">Caminho para um arquivo/diretório existente.</span><span class="sxs-lookup"><span data-stu-id="02bd5-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="02bd5-146">-Recursivo</span><span class="sxs-lookup"><span data-stu-id="02bd5-146">-Recursive</span></span>
<span data-ttu-id="02bd5-147">A lista lida com recursivamente.</span><span class="sxs-lookup"><span data-stu-id="02bd5-147">List handles Recursively.</span></span>
<span data-ttu-id="02bd5-148">Funciona apenas no Diretório de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="02bd5-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="02bd5-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02bd5-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02bd5-150">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="02bd5-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="02bd5-151">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="02bd5-151">-Share</span></span>
<span data-ttu-id="02bd5-152">O objeto CloudFileShare indicou o compartilhamento onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="02bd5-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02bd5-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="02bd5-153">-ShareName</span></span>
<span data-ttu-id="02bd5-154">Nome do compartilhamento de arquivos onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="02bd5-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02bd5-155">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="02bd5-155">-Confirm</span></span>
<span data-ttu-id="02bd5-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02bd5-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02bd5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02bd5-157">-WhatIf</span></span>
<span data-ttu-id="02bd5-158">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="02bd5-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02bd5-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02bd5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02bd5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02bd5-160">CommonParameters</span></span>
<span data-ttu-id="02bd5-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02bd5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02bd5-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02bd5-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02bd5-163">Entradas</span><span class="sxs-lookup"><span data-stu-id="02bd5-163">INPUTS</span></span>

### <span data-ttu-id="02bd5-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="02bd5-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="02bd5-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="02bd5-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="02bd5-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="02bd5-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02bd5-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="02bd5-167">OUTPUTS</span></span>

### <span data-ttu-id="02bd5-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="02bd5-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="02bd5-169">Notas</span><span class="sxs-lookup"><span data-stu-id="02bd5-169">NOTES</span></span>

## <span data-ttu-id="02bd5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02bd5-170">RELATED LINKS</span></span>
