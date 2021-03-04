---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 4badbfc9973b20869c6db421bd1299e00337d7fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890296"
---
# <span data-ttu-id="329f1-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="329f1-101">Update-AzGallery</span></span>

## <span data-ttu-id="329f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="329f1-102">SYNOPSIS</span></span>
<span data-ttu-id="329f1-103">Atualize uma galeria.</span><span class="sxs-lookup"><span data-stu-id="329f1-103">Update a gallery.</span></span>

## <span data-ttu-id="329f1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="329f1-104">SYNTAX</span></span>

### <span data-ttu-id="329f1-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="329f1-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329f1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="329f1-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329f1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="329f1-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329f1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="329f1-108">DESCRIPTION</span></span>
<span data-ttu-id="329f1-109">Atualize uma galeria.</span><span class="sxs-lookup"><span data-stu-id="329f1-109">Update a gallery.</span></span>

## <span data-ttu-id="329f1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="329f1-110">EXAMPLES</span></span>

### <span data-ttu-id="329f1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="329f1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="329f1-112">Atualize uma galeria.</span><span class="sxs-lookup"><span data-stu-id="329f1-112">Update a gallery.</span></span>

## <span data-ttu-id="329f1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="329f1-113">PARAMETERS</span></span>

### <span data-ttu-id="329f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="329f1-114">-AsJob</span></span>
<span data-ttu-id="329f1-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="329f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="329f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329f1-116">-DefaultProfile</span></span>
<span data-ttu-id="329f1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="329f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329f1-118">-Description</span><span class="sxs-lookup"><span data-stu-id="329f1-118">-Description</span></span>
<span data-ttu-id="329f1-119">A descrição do recurso galeria.</span><span class="sxs-lookup"><span data-stu-id="329f1-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="329f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="329f1-120">-InputObject</span></span>
<span data-ttu-id="329f1-121">O objeto PS Gallery.</span><span class="sxs-lookup"><span data-stu-id="329f1-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="329f1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="329f1-122">-Name</span></span>
<span data-ttu-id="329f1-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="329f1-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="329f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="329f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="329f1-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="329f1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="329f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="329f1-126">-ResourceId</span></span>
<span data-ttu-id="329f1-127">A ID do recurso para a galeria</span><span class="sxs-lookup"><span data-stu-id="329f1-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="329f1-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="329f1-128">-Tag</span></span>
<span data-ttu-id="329f1-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="329f1-129">Resource tags</span></span>

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

### <span data-ttu-id="329f1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="329f1-130">-Confirm</span></span>
<span data-ttu-id="329f1-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="329f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329f1-132">-WhatIf</span></span>
<span data-ttu-id="329f1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="329f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329f1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="329f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329f1-135">CommonParameters</span></span>
<span data-ttu-id="329f1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="329f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329f1-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="329f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329f1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="329f1-138">INPUTS</span></span>

### <span data-ttu-id="329f1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="329f1-139">System.String</span></span>

### <span data-ttu-id="329f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="329f1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="329f1-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="329f1-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="329f1-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="329f1-142">OUTPUTS</span></span>

### <span data-ttu-id="329f1-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="329f1-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="329f1-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="329f1-144">NOTES</span></span>

## <span data-ttu-id="329f1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="329f1-145">RELATED LINKS</span></span>
