---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115661"
---
# <span data-ttu-id="9d669-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9d669-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="9d669-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d669-102">SYNOPSIS</span></span>
<span data-ttu-id="9d669-103">Mover um arquivo ou diretório para outro um arquivo ou diretório na mesma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d669-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="9d669-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d669-104">SYNTAX</span></span>

### <span data-ttu-id="9d669-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9d669-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d669-106">ItemEsqueleque</span><span class="sxs-lookup"><span data-stu-id="9d669-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d669-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d669-107">DESCRIPTION</span></span>
<span data-ttu-id="9d669-108">O cmdlet **Mover-AzDataLakeGen2Item** move um arquivo ou diretório para outro um arquivo ou diretório na mesma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d669-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="9d669-109">Esse cmdlet só funcionará se o Namespace Hierárquico estiver habilitado para a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9d669-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="9d669-110">Esse tipo de conta pode ser criado por meio do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="9d669-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="9d669-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9d669-111">EXAMPLES</span></span>

### <span data-ttu-id="9d669-112">Exemplo 1: Mover uma dobra no mesmo sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="9d669-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="9d669-113">Este comando move o diretório 'dir1' para o diretório 'dir3' no mesmo sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d669-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="9d669-114">Exemplo 2: Mover um arquivo por pipeline para outro sistema de arquivos na mesma conta de Armazenamento sem aviso</span><span class="sxs-lookup"><span data-stu-id="9d669-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="9d669-115">Este comando move o arquivo 'dir1/file1' em 'filesystem1' para o arquivo 'dir2/file2' em 'filesystem2' na mesma conta de Armazenamento sem aviso.</span><span class="sxs-lookup"><span data-stu-id="9d669-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="9d669-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d669-116">PARAMETERS</span></span>

### <span data-ttu-id="9d669-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9d669-117">-Context</span></span>
<span data-ttu-id="9d669-118">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9d669-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="9d669-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d669-119">-DefaultProfile</span></span>
<span data-ttu-id="9d669-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d669-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d669-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="9d669-121">-DestFileSystem</span></span>
<span data-ttu-id="9d669-122">Dest FileSystem name</span><span class="sxs-lookup"><span data-stu-id="9d669-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="9d669-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="9d669-123">-DestPath</span></span>
<span data-ttu-id="9d669-124">Caminho Dest Blob</span><span class="sxs-lookup"><span data-stu-id="9d669-124">Dest Blob path</span></span>

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

### <span data-ttu-id="9d669-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9d669-125">-FileSystem</span></span>
<span data-ttu-id="9d669-126">Nome do Sistema de Arquivos</span><span class="sxs-lookup"><span data-stu-id="9d669-126">FileSystem name</span></span>

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

### <span data-ttu-id="9d669-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9d669-127">-Force</span></span>
<span data-ttu-id="9d669-128">Forçar a escrever mais do que o destino.</span><span class="sxs-lookup"><span data-stu-id="9d669-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="9d669-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d669-129">-InputObject</span></span>
<span data-ttu-id="9d669-130">Objeto de Item do Azure Datalake Gen2 para mover-se.</span><span class="sxs-lookup"><span data-stu-id="9d669-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="9d669-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9d669-131">-Path</span></span>
<span data-ttu-id="9d669-132">O caminho no sistema de arquivos especificado que deve ser se mover.</span><span class="sxs-lookup"><span data-stu-id="9d669-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="9d669-133">Pode ser um arquivo ou diretório no formato "diretório/file.txt" ou "diretório1/diretório2/"</span><span class="sxs-lookup"><span data-stu-id="9d669-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="9d669-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9d669-134">-Confirm</span></span>
<span data-ttu-id="9d669-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d669-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d669-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d669-136">-WhatIf</span></span>
<span data-ttu-id="9d669-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9d669-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d669-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d669-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d669-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d669-139">CommonParameters</span></span>
<span data-ttu-id="9d669-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d669-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d669-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d669-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d669-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="9d669-142">INPUTS</span></span>

### <span data-ttu-id="9d669-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9d669-143">System.String</span></span>

### <span data-ttu-id="9d669-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9d669-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="9d669-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9d669-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9d669-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="9d669-146">OUTPUTS</span></span>

### <span data-ttu-id="9d669-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9d669-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="9d669-148">Notas</span><span class="sxs-lookup"><span data-stu-id="9d669-148">NOTES</span></span>

## <span data-ttu-id="9d669-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d669-149">RELATED LINKS</span></span>
