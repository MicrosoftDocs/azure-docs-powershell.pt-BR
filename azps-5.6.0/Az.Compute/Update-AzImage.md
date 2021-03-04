---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: edf0ce1b67c25b8f5e48282dba45e845820c7b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887812"
---
# <span data-ttu-id="7904f-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7904f-101">Update-AzImage</span></span>

## <span data-ttu-id="7904f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7904f-102">SYNOPSIS</span></span>
<span data-ttu-id="7904f-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7904f-103">Updates an image.</span></span>

## <span data-ttu-id="7904f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7904f-104">SYNTAX</span></span>

### <span data-ttu-id="7904f-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7904f-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7904f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7904f-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7904f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7904f-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7904f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7904f-108">DESCRIPTION</span></span>
<span data-ttu-id="7904f-109">O cmdlet **Update-AzImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7904f-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="7904f-110">Atualmente, somente as Marcas podem ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7904f-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="7904f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7904f-111">EXAMPLES</span></span>

### <span data-ttu-id="7904f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7904f-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="7904f-113">Este comando atualiza o valor Tag da imagem existente 'Image01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="7904f-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7904f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7904f-114">PARAMETERS</span></span>

### <span data-ttu-id="7904f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7904f-115">-AsJob</span></span>
<span data-ttu-id="7904f-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7904f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7904f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7904f-117">-DefaultProfile</span></span>
<span data-ttu-id="7904f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7904f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7904f-119">-Image</span><span class="sxs-lookup"><span data-stu-id="7904f-119">-Image</span></span>
<span data-ttu-id="7904f-120">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="7904f-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7904f-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7904f-121">-ImageName</span></span>
<span data-ttu-id="7904f-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7904f-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7904f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7904f-123">-ResourceGroupName</span></span>
<span data-ttu-id="7904f-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7904f-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7904f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7904f-125">-ResourceId</span></span>
<span data-ttu-id="7904f-126">A ID do recurso para a imagem</span><span class="sxs-lookup"><span data-stu-id="7904f-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7904f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="7904f-127">-Tag</span></span>
<span data-ttu-id="7904f-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="7904f-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7904f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7904f-129">-Confirm</span></span>
<span data-ttu-id="7904f-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7904f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7904f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7904f-131">-WhatIf</span></span>
<span data-ttu-id="7904f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7904f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7904f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7904f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7904f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7904f-134">CommonParameters</span></span>
<span data-ttu-id="7904f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7904f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7904f-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7904f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7904f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7904f-137">INPUTS</span></span>

### <span data-ttu-id="7904f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7904f-138">System.String</span></span>

### <span data-ttu-id="7904f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="7904f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7904f-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7904f-140">OUTPUTS</span></span>

### <span data-ttu-id="7904f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="7904f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7904f-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="7904f-142">NOTES</span></span>

## <span data-ttu-id="7904f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7904f-143">RELATED LINKS</span></span>
