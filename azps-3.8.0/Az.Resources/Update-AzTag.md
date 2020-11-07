---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: b41f7ca642d74a33c239f125d7dfe2ccdbad1b68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777635"
---
# <span data-ttu-id="27c89-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="27c89-101">Update-AzTag</span></span>

## <span data-ttu-id="27c89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27c89-102">SYNOPSIS</span></span>

<span data-ttu-id="27c89-103">Atualiza seletivamente o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="27c89-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="27c89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27c89-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="27c89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27c89-105">DESCRIPTION</span></span>

<span data-ttu-id="27c89-106">O cmdlet **Update-AzTag** com uma **ResourceId** atualiza seletivamente o conjunto de marcas em um recurso ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="27c89-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="27c89-107">Esta operação permite substituir, mesclar ou excluir seletivamente marcas no recurso ou assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="27c89-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="27c89-108">A entidade especificada pode ter no máximo 50 marcas no final da operação.</span><span class="sxs-lookup"><span data-stu-id="27c89-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="27c89-109">A opção ' substituir ' substitui todo o conjunto de marcas existentes por um novo conjunto.</span><span class="sxs-lookup"><span data-stu-id="27c89-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="27c89-110">A opção "Mesclar" permite adicionar marcas com novos nomes e atualizar os valores das marcas com nomes existentes.</span><span class="sxs-lookup"><span data-stu-id="27c89-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="27c89-111">A opção ' excluir ' permite excluir marcas seletivamente com base em determinados nomes ou pares de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="27c89-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="27c89-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27c89-112">EXAMPLES</span></span>

### <span data-ttu-id="27c89-113">Exemplo 1: atualiza seletivamente o conjunto de marcas em uma assinatura com operação de "Mesclar"</span><span class="sxs-lookup"><span data-stu-id="27c89-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="27c89-114">Esse comando mescla o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="27c89-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="27c89-115">Exemplo 2: atualiza seletivamente o conjunto de marcas em uma assinatura com a operação "Replace"</span><span class="sxs-lookup"><span data-stu-id="27c89-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="27c89-116">Este comando Repalces o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="27c89-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="27c89-117">Exemplo 3: atualiza seletivamente o conjunto de marcas em uma assinatura com a operação "excluir"</span><span class="sxs-lookup"><span data-stu-id="27c89-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="27c89-118">Este comando exclui o conjunto de marcas na assinatura com {subId}.</span><span class="sxs-lookup"><span data-stu-id="27c89-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="27c89-119">OS</span><span class="sxs-lookup"><span data-stu-id="27c89-119">PARAMETERS</span></span>

### <span data-ttu-id="27c89-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c89-120">-DefaultProfile</span></span>
<span data-ttu-id="27c89-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27c89-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27c89-122">-ResourceId</span></span>
<span data-ttu-id="27c89-123">O identificador de recurso para a entidade marcada.</span><span class="sxs-lookup"><span data-stu-id="27c89-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="27c89-124">Um recurso, um grupo de recursos ou uma assinatura pode estar marcado.</span><span class="sxs-lookup"><span data-stu-id="27c89-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="27c89-125">-Tag</span></span>
<span data-ttu-id="27c89-126">O conjunto de marcas a serem usadas para atualização.</span><span class="sxs-lookup"><span data-stu-id="27c89-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-127">-Operação</span><span class="sxs-lookup"><span data-stu-id="27c89-127">-Operation</span></span>
<span data-ttu-id="27c89-128">A operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="27c89-128">The update operation.</span></span> <span data-ttu-id="27c89-129">As opções são mesclar, substituir e excluir.</span><span class="sxs-lookup"><span data-stu-id="27c89-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27c89-130">-Confirm</span></span>
<span data-ttu-id="27c89-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c89-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c89-132">-WhatIf</span></span>
<span data-ttu-id="27c89-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27c89-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c89-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27c89-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c89-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c89-135">CommonParameters</span></span>
<span data-ttu-id="27c89-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c89-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c89-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27c89-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c89-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27c89-138">INPUTS</span></span>

### <span data-ttu-id="27c89-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27c89-139">System.String</span></span>

### <span data-ttu-id="27c89-140">Microsoft. Azure. Commands. Tags. Model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="27c89-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="27c89-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="27c89-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27c89-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27c89-142">OUTPUTS</span></span>

### <span data-ttu-id="27c89-143">Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="27c89-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="27c89-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27c89-144">NOTES</span></span>

## <span data-ttu-id="27c89-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27c89-145">RELATED LINKS</span></span>

[<span data-ttu-id="27c89-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="27c89-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="27c89-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="27c89-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="27c89-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="27c89-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
