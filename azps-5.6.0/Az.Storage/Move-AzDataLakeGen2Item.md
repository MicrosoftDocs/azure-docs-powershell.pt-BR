---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: 203e7a246c16345631da290645b356392c165bad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888784"
---
# <span data-ttu-id="b0953-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b0953-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="b0953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0953-102">SYNOPSIS</span></span>
<span data-ttu-id="b0953-103">Mova um arquivo ou diretório para outro arquivo ou diretório na mesma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0953-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="b0953-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0953-104">SYNTAX</span></span>

### <span data-ttu-id="b0953-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b0953-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0953-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="b0953-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0953-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0953-107">DESCRIPTION</span></span>
<span data-ttu-id="b0953-108">O cmdlet **Move-AzDataLakeGen2Item** move um arquivo ou diretório para outro arquivo ou diretório na mesma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0953-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="b0953-109">Esse cmdlet só funcionará se Namespace Hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0953-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b0953-110">Esse tipo de conta pode ser criada com o cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="b0953-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b0953-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0953-111">EXAMPLES</span></span>

### <span data-ttu-id="b0953-112">Exemplo 1: mover uma dobra no mesmo sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0953-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="b0953-113">Este comando move o diretório 'dir1' para o diretório 'dir3' no mesmo Sistema de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0953-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="b0953-114">Exemplo 2: mover um arquivo por pipeline para outro sistema de arquivos na mesma conta de Armazenamento sem prompt</span><span class="sxs-lookup"><span data-stu-id="b0953-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="b0953-115">Este arquivo de movimentação de comando 'dir1/file1' em 'filesystem1' para o arquivo 'dir2/file2' em 'filesystem2' na mesma conta de Armazenamento sem prompt.</span><span class="sxs-lookup"><span data-stu-id="b0953-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="b0953-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0953-116">PARAMETERS</span></span>

### <span data-ttu-id="b0953-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b0953-117">-Context</span></span>
<span data-ttu-id="b0953-118">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="b0953-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b0953-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0953-119">-DefaultProfile</span></span>
<span data-ttu-id="b0953-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0953-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0953-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="b0953-121">-DestFileSystem</span></span>
<span data-ttu-id="b0953-122">Nome do FileSystem dest</span><span class="sxs-lookup"><span data-stu-id="b0953-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0953-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="b0953-123">-DestPath</span></span>
<span data-ttu-id="b0953-124">Dest Blob path</span><span class="sxs-lookup"><span data-stu-id="b0953-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0953-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b0953-125">-FileSystem</span></span>
<span data-ttu-id="b0953-126">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="b0953-126">FileSystem name</span></span>

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

### <span data-ttu-id="b0953-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b0953-127">-Force</span></span>
<span data-ttu-id="b0953-128">Force a gravar mais o destino.</span><span class="sxs-lookup"><span data-stu-id="b0953-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="b0953-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0953-129">-InputObject</span></span>
<span data-ttu-id="b0953-130">Objeto de item do Azure Datalake Gen2 para mover.</span><span class="sxs-lookup"><span data-stu-id="b0953-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="b0953-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b0953-131">-Path</span></span>
<span data-ttu-id="b0953-132">O caminho no sistema de arquivos especificado que deve ser movimentado.</span><span class="sxs-lookup"><span data-stu-id="b0953-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="b0953-133">Pode ser um arquivo ou diretório No formato 'directory/file.txt' ou 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="b0953-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0953-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0953-134">-Confirm</span></span>
<span data-ttu-id="b0953-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0953-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0953-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0953-136">-WhatIf</span></span>
<span data-ttu-id="b0953-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0953-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0953-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0953-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0953-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0953-139">CommonParameters</span></span>
<span data-ttu-id="b0953-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0953-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0953-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0953-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0953-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0953-142">INPUTS</span></span>

### <span data-ttu-id="b0953-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b0953-143">System.String</span></span>

### <span data-ttu-id="b0953-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b0953-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="b0953-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0953-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0953-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0953-146">OUTPUTS</span></span>

### <span data-ttu-id="b0953-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b0953-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b0953-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0953-148">NOTES</span></span>

## <span data-ttu-id="b0953-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0953-149">RELATED LINKS</span></span>
