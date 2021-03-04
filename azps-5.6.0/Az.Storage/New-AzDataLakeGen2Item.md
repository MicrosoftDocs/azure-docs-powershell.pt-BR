---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 565267c6f35f52fd3a7a733477ed504d001cb70b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891554"
---
# <span data-ttu-id="cd5d7-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd5d7-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="cd5d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5d7-103">Crie um arquivo ou diretório em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="cd5d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cd5d7-104">SYNTAX</span></span>

### <span data-ttu-id="cd5d7-105">Arquivo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cd5d7-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd5d7-106">Diretório</span><span class="sxs-lookup"><span data-stu-id="cd5d7-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd5d7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cd5d7-107">DESCRIPTION</span></span>
<span data-ttu-id="cd5d7-108">O cmdlet **New-AzDataLakeGen2Item** cria um arquivo ou diretório em um sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="cd5d7-109">Esse cmdlet só funcionará se Namespace Hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="cd5d7-110">Esse tipo de conta pode ser criada com o cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="cd5d7-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="cd5d7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-111">EXAMPLES</span></span>

### <span data-ttu-id="cd5d7-112">Exemplo 1: Criar um diretório com permissão especificada, Umask, propriedades e metadados</span><span class="sxs-lookup"><span data-stu-id="cd5d7-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="cd5d7-113">Este comando cria um diretório com Permissões especificadas, Umask, propriedades e metadados</span><span class="sxs-lookup"><span data-stu-id="cd5d7-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="cd5d7-114">Exemplo 2: Criar(carregar) um arquivo de lago de dados de um arquivo de origem local e o cmdlet é executado em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cd5d7-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="cd5d7-115">Este comando cria(carregar) um arquivo de lago de dados de um arquivo de origem local e o cmdlet é executado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="cd5d7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-116">PARAMETERS</span></span>

### <span data-ttu-id="cd5d7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd5d7-117">-AsJob</span></span>
<span data-ttu-id="cd5d7-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cd5d7-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd5d7-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cd5d7-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cd5d7-120">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="cd5d7-121">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-121">The default value is 10.</span></span>

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

### <span data-ttu-id="cd5d7-122">-Context</span><span class="sxs-lookup"><span data-stu-id="cd5d7-122">-Context</span></span>
<span data-ttu-id="cd5d7-123">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="cd5d7-123">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5d7-124">-DefaultProfile</span></span>
<span data-ttu-id="cd5d7-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5d7-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="cd5d7-126">-Directory</span></span>
<span data-ttu-id="cd5d7-127">Indica que esse novo item é um diretório e não um arquivo.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="cd5d7-128">-FileSystem</span></span>
<span data-ttu-id="cd5d7-129">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="cd5d7-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-130">-Force</span><span class="sxs-lookup"><span data-stu-id="cd5d7-130">-Force</span></span>
<span data-ttu-id="cd5d7-131">Se aprovado, o novo item será criado sem qualquer prompt</span><span class="sxs-lookup"><span data-stu-id="cd5d7-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="cd5d7-132">-Metadados</span><span class="sxs-lookup"><span data-stu-id="cd5d7-132">-Metadata</span></span>
<span data-ttu-id="cd5d7-133">Especifica metadados para o diretório ou arquivo criado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-134">-Path</span><span class="sxs-lookup"><span data-stu-id="cd5d7-134">-Path</span></span>
<span data-ttu-id="cd5d7-135">O caminho no sistema de arquivos especificado que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="cd5d7-136">Pode ser um arquivo ou diretório No formato 'directory/file.txt' ou 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="cd5d7-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="cd5d7-137">-Permission</span></span>
<span data-ttu-id="cd5d7-138">Define permissões de acesso POSIX para o proprietário do arquivo, o grupo proprietário de arquivos e outros.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="cd5d7-139">Cada classe pode ter permissão de leitura, gravação ou execução.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="cd5d7-140">Simbólico (rwxrw-rw-) é suportado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-140">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-141">-Property</span><span class="sxs-lookup"><span data-stu-id="cd5d7-141">-Property</span></span>
<span data-ttu-id="cd5d7-142">Especifica propriedades para o diretório ou arquivo criado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="cd5d7-143">As propriedades suportadas para o arquivo são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="cd5d7-144">As propriedades suportadas para diretório são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-145">-Source</span><span class="sxs-lookup"><span data-stu-id="cd5d7-145">-Source</span></span>
<span data-ttu-id="cd5d7-146">Especifique o caminho do arquivo de origem local que será carregado em um arquivo Datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="cd5d7-147">-Umask</span></span>
<span data-ttu-id="cd5d7-148">Ao criar Novo Item e o diretório pai não tiver uma ACL padrão, a umask restringe as permissões do arquivo ou diretório a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="cd5d7-149">A permissão resultante é dada por p & ^u, onde p é a permissão e você é a umask.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="cd5d7-150">Simbólico (rwxrw-rw-) é suportado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-150">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d7-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd5d7-151">-Confirm</span></span>
<span data-ttu-id="cd5d7-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd5d7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd5d7-153">-WhatIf</span></span>
<span data-ttu-id="cd5d7-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd5d7-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd5d7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5d7-156">CommonParameters</span></span>
<span data-ttu-id="cd5d7-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5d7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5d7-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd5d7-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5d7-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-159">INPUTS</span></span>

### <span data-ttu-id="cd5d7-160">System.String</span><span class="sxs-lookup"><span data-stu-id="cd5d7-160">System.String</span></span>

### <span data-ttu-id="cd5d7-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd5d7-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd5d7-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-162">OUTPUTS</span></span>

### <span data-ttu-id="cd5d7-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd5d7-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="cd5d7-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="cd5d7-164">NOTES</span></span>

## <span data-ttu-id="cd5d7-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd5d7-165">RELATED LINKS</span></span>
