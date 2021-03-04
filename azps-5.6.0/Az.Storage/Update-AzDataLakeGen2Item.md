---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: fdcac32a925cad97c256af2db949a08268e0ac3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886302"
---
# <span data-ttu-id="7adb6-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7adb6-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="7adb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adb6-102">SYNOPSIS</span></span>
<span data-ttu-id="7adb6-103">Atualize um arquivo ou diretório em propriedades, metadados, permissão, ACL e proprietário.</span><span class="sxs-lookup"><span data-stu-id="7adb6-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="7adb6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7adb6-104">SYNTAX</span></span>

### <span data-ttu-id="7adb6-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7adb6-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7adb6-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="7adb6-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7adb6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7adb6-107">DESCRIPTION</span></span>
<span data-ttu-id="7adb6-108">O cmdlet **Update-AzDataLakeGen2Item** atualiza um arquivo ou diretório em propriedades, metadados, permissão, ACL e proprietário.</span><span class="sxs-lookup"><span data-stu-id="7adb6-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="7adb6-109">Esse cmdlet só funcionará se Namespace Hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7adb6-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="7adb6-110">Esse tipo de conta pode ser criada com o cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="7adb6-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="7adb6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7adb6-111">EXAMPLES</span></span>

### <span data-ttu-id="7adb6-112">Exemplo 1: Criar um objeto ACL com entrada 3 ACL e atualizar a ACL para todos os itens em um sistema de arquivos recursivamente</span><span class="sxs-lookup"><span data-stu-id="7adb6-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="7adb6-113">Este comando primeiro cria um objeto ACL com entrada de 3 acl (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span><span class="sxs-lookup"><span data-stu-id="7adb6-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="7adb6-114">Exemplo 2: atualizar todas as propriedades em um arquivo e mostrar a eles</span><span class="sxs-lookup"><span data-stu-id="7adb6-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="7adb6-115">Este comando atualiza todas as propriedades em um arquivo (ACL, permission,owner, group, metadata, property can be updated with any conbination) and show them in Powershell console.</span><span class="sxs-lookup"><span data-stu-id="7adb6-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="7adb6-116">Exemplo 3: Adicionar uma entrada ACL a um diretório</span><span class="sxs-lookup"><span data-stu-id="7adb6-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="7adb6-117">Este comando obtém a ACL de um diretório, atualiza/adiciona uma entrada ACL e define de volta ao diretório.</span><span class="sxs-lookup"><span data-stu-id="7adb6-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="7adb6-118">Se a entrada ACL com o mesmo AccessControlType/EntityId/DefaultScope não existir, adicionará uma nova entrada ACL, ou atualizará a permissão da entrada ACL existente.</span><span class="sxs-lookup"><span data-stu-id="7adb6-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="7adb6-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7adb6-119">PARAMETERS</span></span>

### <span data-ttu-id="7adb6-120">-Acl</span><span class="sxs-lookup"><span data-stu-id="7adb6-120">-Acl</span></span>
<span data-ttu-id="7adb6-121">Define direitos de controle de acesso POSIX em arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="7adb6-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="7adb6-122">Crie este objeto com New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="7adb6-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adb6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="7adb6-123">-Context</span></span>
<span data-ttu-id="7adb6-124">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="7adb6-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7adb6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adb6-125">-DefaultProfile</span></span>
<span data-ttu-id="7adb6-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7adb6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adb6-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7adb6-127">-FileSystem</span></span>
<span data-ttu-id="7adb6-128">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="7adb6-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adb6-129">-Group</span><span class="sxs-lookup"><span data-stu-id="7adb6-129">-Group</span></span>
<span data-ttu-id="7adb6-130">Define o grupo de propriedade do blob.</span><span class="sxs-lookup"><span data-stu-id="7adb6-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="7adb6-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7adb6-131">-InputObject</span></span>
<span data-ttu-id="7adb6-132">Objeto de item do Azure Datalake Gen2 para atualizar</span><span class="sxs-lookup"><span data-stu-id="7adb6-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adb6-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7adb6-133">-Metadata</span></span>
<span data-ttu-id="7adb6-134">Especifica metadados para o diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="7adb6-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="7adb6-135">-Owner</span><span class="sxs-lookup"><span data-stu-id="7adb6-135">-Owner</span></span>
<span data-ttu-id="7adb6-136">Define o proprietário do blob.</span><span class="sxs-lookup"><span data-stu-id="7adb6-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="7adb6-137">-Path</span><span class="sxs-lookup"><span data-stu-id="7adb6-137">-Path</span></span>
<span data-ttu-id="7adb6-138">O caminho no sistema de arquivos especificado que deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="7adb6-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="7adb6-139">Pode ser um arquivo ou diretório No formato 'directory/file.txt' ou 'directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="7adb6-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="7adb6-140">Não especificar esse parâmetro atualizará o diretório raiz do Sistema de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="7adb6-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adb6-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="7adb6-141">-Permission</span></span>
<span data-ttu-id="7adb6-142">Define permissões de acesso POSIX para o proprietário do arquivo, o grupo proprietário de arquivos e outros.</span><span class="sxs-lookup"><span data-stu-id="7adb6-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="7adb6-143">Cada classe pode ter permissão de leitura, gravação ou execução.</span><span class="sxs-lookup"><span data-stu-id="7adb6-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="7adb6-144">Simbólico (rwxrw-rw-) é suportado.</span><span class="sxs-lookup"><span data-stu-id="7adb6-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="7adb6-145">Inválido em conjunto com a Acl.</span><span class="sxs-lookup"><span data-stu-id="7adb6-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="7adb6-146">-Property</span><span class="sxs-lookup"><span data-stu-id="7adb6-146">-Property</span></span>
<span data-ttu-id="7adb6-147">Especifica propriedades para o diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="7adb6-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="7adb6-148">As propriedades suportadas para o arquivo são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="7adb6-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="7adb6-149">As propriedades suportadas para diretório são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="7adb6-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="7adb6-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7adb6-150">-Confirm</span></span>
<span data-ttu-id="7adb6-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7adb6-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adb6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adb6-152">-WhatIf</span></span>
<span data-ttu-id="7adb6-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7adb6-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7adb6-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7adb6-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adb6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adb6-155">CommonParameters</span></span>
<span data-ttu-id="7adb6-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adb6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adb6-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adb6-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adb6-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7adb6-158">INPUTS</span></span>

### <span data-ttu-id="7adb6-159">System.String</span><span class="sxs-lookup"><span data-stu-id="7adb6-159">System.String</span></span>

### <span data-ttu-id="7adb6-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7adb6-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="7adb6-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7adb6-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7adb6-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7adb6-162">OUTPUTS</span></span>

### <span data-ttu-id="7adb6-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7adb6-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="7adb6-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="7adb6-164">NOTES</span></span>

## <span data-ttu-id="7adb6-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7adb6-165">RELATED LINKS</span></span>
