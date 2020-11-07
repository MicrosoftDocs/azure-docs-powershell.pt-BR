---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944676"
---
# <span data-ttu-id="98b4b-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="98b4b-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="98b4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="98b4b-103">Remover um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="98b4b-103">Remove a file or directory.</span></span>

## <span data-ttu-id="98b4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98b4b-104">SYNTAX</span></span>

### <span data-ttu-id="98b4b-105">ReceiveManual (padrão)</span><span class="sxs-lookup"><span data-stu-id="98b4b-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98b4b-106">Hiperencanamento</span><span class="sxs-lookup"><span data-stu-id="98b4b-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98b4b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98b4b-107">DESCRIPTION</span></span>
<span data-ttu-id="98b4b-108">O cmdlet **Remove-AzDataLakeGen2Item** remove um arquivo ou diretório de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98b4b-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="98b4b-109">Este cmdlet só funcionará se o namespace hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98b4b-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="98b4b-110">Esse tipo de conta pode ser criado por meio da execução do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="98b4b-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="98b4b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98b4b-111">EXAMPLES</span></span>

### <span data-ttu-id="98b4b-112">Exemplo 1: Remove um diretório</span><span class="sxs-lookup"><span data-stu-id="98b4b-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="98b4b-113">Esse comando Remove um diretório de um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="98b4b-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="98b4b-114">Exemplo 2: Remove um arquivo sem perguntar</span><span class="sxs-lookup"><span data-stu-id="98b4b-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="98b4b-115">Esse comando Remove um diretório de um sistema de arquivos, sem solicitação.</span><span class="sxs-lookup"><span data-stu-id="98b4b-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="98b4b-116">Exemplo 3: remover todos os itens de um sistema de arquivos com pipeline</span><span class="sxs-lookup"><span data-stu-id="98b4b-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="98b4b-117">Esse comando Remove todos os itens de um sistema de arquivos com pipeline.</span><span class="sxs-lookup"><span data-stu-id="98b4b-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="98b4b-118">OS</span><span class="sxs-lookup"><span data-stu-id="98b4b-118">PARAMETERS</span></span>

### <span data-ttu-id="98b4b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98b4b-119">-AsJob</span></span>
<span data-ttu-id="98b4b-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="98b4b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98b4b-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="98b4b-121">-Context</span></span>
<span data-ttu-id="98b4b-122">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="98b4b-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="98b4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b4b-123">-DefaultProfile</span></span>
<span data-ttu-id="98b4b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98b4b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98b4b-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="98b4b-125">-FileSystem</span></span>
<span data-ttu-id="98b4b-126">Nome do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="98b4b-126">FileSystem name</span></span>

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

### <span data-ttu-id="98b4b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="98b4b-127">-Force</span></span>
<span data-ttu-id="98b4b-128">Forçar a remoção do sistema de arquivos e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="98b4b-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="98b4b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b4b-129">-InputObject</span></span>
<span data-ttu-id="98b4b-130">Objeto de item Gen2 do Azure datalake para remoção.</span><span class="sxs-lookup"><span data-stu-id="98b4b-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="98b4b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98b4b-131">-PassThru</span></span>
<span data-ttu-id="98b4b-132">Retorna se o sistema de arquivos especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="98b4b-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="98b4b-133">-Caminho</span><span class="sxs-lookup"><span data-stu-id="98b4b-133">-Path</span></span>
<span data-ttu-id="98b4b-134">O caminho no sistema de arquivos especificado que deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="98b4b-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="98b4b-135">Pode ser um arquivo ou diretório no formato ' diretório/file.txt ' ou ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="98b4b-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="98b4b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98b4b-136">-Confirm</span></span>
<span data-ttu-id="98b4b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98b4b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b4b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b4b-138">-WhatIf</span></span>
<span data-ttu-id="98b4b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b4b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b4b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b4b-141">CommonParameters</span></span>
<span data-ttu-id="98b4b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b4b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b4b-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b4b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b4b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98b4b-144">INPUTS</span></span>

### <span data-ttu-id="98b4b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="98b4b-145">System.String</span></span>

### <span data-ttu-id="98b4b-146">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="98b4b-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="98b4b-147">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98b4b-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98b4b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98b4b-148">OUTPUTS</span></span>

### <span data-ttu-id="98b4b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98b4b-149">System.Boolean</span></span>

## <span data-ttu-id="98b4b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98b4b-150">NOTES</span></span>

## <span data-ttu-id="98b4b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98b4b-151">RELATED LINKS</span></span>
