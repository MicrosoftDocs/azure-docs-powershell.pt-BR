---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114435"
---
# <span data-ttu-id="8a718-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="8a718-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="8a718-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a718-102">SYNOPSIS</span></span>
<span data-ttu-id="8a718-103">Criar um arquivo ou diretório em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8a718-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="8a718-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a718-104">SYNTAX</span></span>

### <span data-ttu-id="8a718-105">Arquivo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a718-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a718-106">Diretório</span><span class="sxs-lookup"><span data-stu-id="8a718-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a718-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a718-107">DESCRIPTION</span></span>
<span data-ttu-id="8a718-108">O cmdlet **New-AzDataLakeGen2Item** cria um arquivo ou diretório em um sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a718-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="8a718-109">Esse cmdlet só funcionará se o Namespace Hierárquico estiver habilitado para a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8a718-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="8a718-110">Esse tipo de conta pode ser criado por meio do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="8a718-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="8a718-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a718-111">EXAMPLES</span></span>

### <span data-ttu-id="8a718-112">Exemplo 1: Criar um diretório com permissão especificada, Umask, propriedades e metadados</span><span class="sxs-lookup"><span data-stu-id="8a718-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="8a718-113">Esse comando cria um diretório com Permissão especificada, Umask, propriedades e metadados</span><span class="sxs-lookup"><span data-stu-id="8a718-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="8a718-114">Exemplo 2: Criar(carregar) um arquivo de lago de dados de um arquivo de origem local e o cmdlet é executado em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a718-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="8a718-115">Esse comando cria(carregar) um arquivo de lago de dados de um arquivo de origem local e o cmdlet é executado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8a718-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="8a718-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a718-116">PARAMETERS</span></span>

### <span data-ttu-id="8a718-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a718-117">-AsJob</span></span>
<span data-ttu-id="8a718-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a718-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a718-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8a718-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8a718-120">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8a718-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="8a718-121">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="8a718-121">The default value is 10.</span></span>

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

### <span data-ttu-id="8a718-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8a718-122">-Context</span></span>
<span data-ttu-id="8a718-123">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="8a718-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8a718-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a718-124">-DefaultProfile</span></span>
<span data-ttu-id="8a718-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a718-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a718-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="8a718-126">-Directory</span></span>
<span data-ttu-id="8a718-127">Indica que esse novo item é um diretório e não um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a718-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="8a718-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8a718-128">-FileSystem</span></span>
<span data-ttu-id="8a718-129">Nome do Sistema de Arquivos</span><span class="sxs-lookup"><span data-stu-id="8a718-129">FileSystem name</span></span>

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

### <span data-ttu-id="8a718-130">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8a718-130">-Force</span></span>
<span data-ttu-id="8a718-131">Se aprovado, um novo item será criado sem qualquer aviso</span><span class="sxs-lookup"><span data-stu-id="8a718-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="8a718-132">-Metadados</span><span class="sxs-lookup"><span data-stu-id="8a718-132">-Metadata</span></span>
<span data-ttu-id="8a718-133">Especifica metadados para o diretório ou arquivo criado.</span><span class="sxs-lookup"><span data-stu-id="8a718-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="8a718-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8a718-134">-Path</span></span>
<span data-ttu-id="8a718-135">O caminho no sistema de arquivos especificado que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8a718-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="8a718-136">Pode ser um arquivo ou diretório no formato "diretório/file.txt" ou "diretório1/diretório2/"</span><span class="sxs-lookup"><span data-stu-id="8a718-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="8a718-137">-Permissão</span><span class="sxs-lookup"><span data-stu-id="8a718-137">-Permission</span></span>
<span data-ttu-id="8a718-138">Define permissões de acesso POSIX para o proprietário do arquivo, o grupo proprietário de arquivos e outros.</span><span class="sxs-lookup"><span data-stu-id="8a718-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="8a718-139">Cada classe pode ter permissão de leitura, gravação ou execução.</span><span class="sxs-lookup"><span data-stu-id="8a718-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="8a718-140">Há suporte para símbolos (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="8a718-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="8a718-141">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="8a718-141">-Property</span></span>
<span data-ttu-id="8a718-142">Especifica as propriedades do diretório ou arquivo criado.</span><span class="sxs-lookup"><span data-stu-id="8a718-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="8a718-143">As propriedades com suporte para o arquivo são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="8a718-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="8a718-144">As propriedades com suporte para diretório são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="8a718-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="8a718-145">-Origem</span><span class="sxs-lookup"><span data-stu-id="8a718-145">-Source</span></span>
<span data-ttu-id="8a718-146">Especifique o caminho do arquivo de origem local que será carregado para um arquivo Datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="8a718-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="8a718-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="8a718-147">-Umask</span></span>
<span data-ttu-id="8a718-148">Ao criar Novo Item e o diretório pai não tiver um ACL padrão, o umask restringirá as permissões do arquivo ou diretório a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8a718-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="8a718-149">A permissão resultante é concedida por p & ^u, onde p é a permissão e você é a umask.</span><span class="sxs-lookup"><span data-stu-id="8a718-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="8a718-150">Há suporte para símbolos (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="8a718-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="8a718-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8a718-151">-Confirm</span></span>
<span data-ttu-id="8a718-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a718-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a718-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a718-153">-WhatIf</span></span>
<span data-ttu-id="8a718-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8a718-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a718-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a718-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a718-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a718-156">CommonParameters</span></span>
<span data-ttu-id="8a718-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a718-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a718-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a718-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a718-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a718-159">INPUTS</span></span>

### <span data-ttu-id="8a718-160">System.String</span><span class="sxs-lookup"><span data-stu-id="8a718-160">System.String</span></span>

### <span data-ttu-id="8a718-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a718-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a718-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a718-162">OUTPUTS</span></span>

### <span data-ttu-id="8a718-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="8a718-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="8a718-164">Notas</span><span class="sxs-lookup"><span data-stu-id="8a718-164">NOTES</span></span>

## <span data-ttu-id="8a718-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a718-165">RELATED LINKS</span></span>
