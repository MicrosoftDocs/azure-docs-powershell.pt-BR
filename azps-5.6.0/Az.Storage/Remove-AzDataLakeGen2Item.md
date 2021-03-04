---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 2d3db18c49d29cabb8f6459adcd46a9c0242c02f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889132"
---
# <span data-ttu-id="192d5-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="192d5-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="192d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="192d5-102">SYNOPSIS</span></span>
<span data-ttu-id="192d5-103">Remova um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="192d5-103">Remove a file or directory.</span></span>

## <span data-ttu-id="192d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="192d5-104">SYNTAX</span></span>

### <span data-ttu-id="192d5-105">ReceiveManual (Padrão)</span><span class="sxs-lookup"><span data-stu-id="192d5-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="192d5-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="192d5-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="192d5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="192d5-107">DESCRIPTION</span></span>
<span data-ttu-id="192d5-108">O cmdlet **Remove-AzDataLakeGen2Item** remove um arquivo ou diretório de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="192d5-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="192d5-109">Esse cmdlet só funcionará se Namespace Hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="192d5-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="192d5-110">Esse tipo de conta pode ser criada com o cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="192d5-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="192d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="192d5-111">EXAMPLES</span></span>

### <span data-ttu-id="192d5-112">Exemplo 1: Remove um diretório</span><span class="sxs-lookup"><span data-stu-id="192d5-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="192d5-113">Este comando remove um diretório de um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="192d5-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="192d5-114">Exemplo 2: Remove um arquivo sem prompt</span><span class="sxs-lookup"><span data-stu-id="192d5-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="192d5-115">Este comando remove um diretório de um sistema de arquivos, sem prompt.</span><span class="sxs-lookup"><span data-stu-id="192d5-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="192d5-116">Exemplo 3: Remover todos os itens em um sistema de arquivos com pipeline</span><span class="sxs-lookup"><span data-stu-id="192d5-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="192d5-117">Este comando remove todos os itens em um sistema de arquivos com pipeline.</span><span class="sxs-lookup"><span data-stu-id="192d5-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="192d5-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="192d5-118">PARAMETERS</span></span>

### <span data-ttu-id="192d5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="192d5-119">-AsJob</span></span>
<span data-ttu-id="192d5-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="192d5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="192d5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="192d5-121">-Context</span></span>
<span data-ttu-id="192d5-122">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="192d5-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="192d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192d5-123">-DefaultProfile</span></span>
<span data-ttu-id="192d5-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="192d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="192d5-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="192d5-125">-FileSystem</span></span>
<span data-ttu-id="192d5-126">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="192d5-126">FileSystem name</span></span>

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

### <span data-ttu-id="192d5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="192d5-127">-Force</span></span>
<span data-ttu-id="192d5-128">Forçar a remover o Sistema de Arquivos e todo o conteúdo nele</span><span class="sxs-lookup"><span data-stu-id="192d5-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="192d5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="192d5-129">-InputObject</span></span>
<span data-ttu-id="192d5-130">Objeto de item do Azure Datalake Gen2 a ser removido.</span><span class="sxs-lookup"><span data-stu-id="192d5-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="192d5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="192d5-131">-PassThru</span></span>
<span data-ttu-id="192d5-132">Retornar se o sistema de arquivos especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="192d5-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="192d5-133">-Path</span><span class="sxs-lookup"><span data-stu-id="192d5-133">-Path</span></span>
<span data-ttu-id="192d5-134">O caminho no sistema de arquivos especificado que deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="192d5-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="192d5-135">Pode ser um arquivo ou diretório No formato 'directory/file.txt' ou 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="192d5-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="192d5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="192d5-136">-Confirm</span></span>
<span data-ttu-id="192d5-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="192d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="192d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="192d5-138">-WhatIf</span></span>
<span data-ttu-id="192d5-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="192d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="192d5-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="192d5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="192d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192d5-141">CommonParameters</span></span>
<span data-ttu-id="192d5-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192d5-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192d5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192d5-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="192d5-144">INPUTS</span></span>

### <span data-ttu-id="192d5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="192d5-145">System.String</span></span>

### <span data-ttu-id="192d5-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="192d5-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="192d5-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="192d5-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="192d5-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="192d5-148">OUTPUTS</span></span>

### <span data-ttu-id="192d5-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="192d5-149">System.Boolean</span></span>

## <span data-ttu-id="192d5-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="192d5-150">NOTES</span></span>

## <span data-ttu-id="192d5-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="192d5-151">RELATED LINKS</span></span>
