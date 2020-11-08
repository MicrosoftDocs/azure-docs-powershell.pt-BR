---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113397"
---
# <span data-ttu-id="12b07-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="12b07-101">Update-AzGallery</span></span>

## <span data-ttu-id="12b07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12b07-102">SYNOPSIS</span></span>
<span data-ttu-id="12b07-103">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="12b07-103">Update a gallery.</span></span>

## <span data-ttu-id="12b07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12b07-104">SYNTAX</span></span>

### <span data-ttu-id="12b07-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="12b07-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b07-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="12b07-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b07-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="12b07-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b07-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12b07-108">DESCRIPTION</span></span>
<span data-ttu-id="12b07-109">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="12b07-109">Update a gallery.</span></span>

## <span data-ttu-id="12b07-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12b07-110">EXAMPLES</span></span>

### <span data-ttu-id="12b07-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12b07-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="12b07-112">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="12b07-112">Update a gallery.</span></span>

## <span data-ttu-id="12b07-113">OS</span><span class="sxs-lookup"><span data-stu-id="12b07-113">PARAMETERS</span></span>

### <span data-ttu-id="12b07-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12b07-114">-AsJob</span></span>
<span data-ttu-id="12b07-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="12b07-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12b07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b07-116">-DefaultProfile</span></span>
<span data-ttu-id="12b07-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12b07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b07-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="12b07-118">-Description</span></span>
<span data-ttu-id="12b07-119">A descrição do recurso de galeria.</span><span class="sxs-lookup"><span data-stu-id="12b07-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="12b07-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12b07-120">-InputObject</span></span>
<span data-ttu-id="12b07-121">O objeto da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="12b07-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="12b07-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="12b07-122">-Name</span></span>
<span data-ttu-id="12b07-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="12b07-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="12b07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b07-124">-ResourceGroupName</span></span>
<span data-ttu-id="12b07-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12b07-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="12b07-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12b07-126">-ResourceId</span></span>
<span data-ttu-id="12b07-127">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="12b07-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="12b07-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="12b07-128">-Tag</span></span>
<span data-ttu-id="12b07-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="12b07-129">Resource tags</span></span>

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

### <span data-ttu-id="12b07-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12b07-130">-Confirm</span></span>
<span data-ttu-id="12b07-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b07-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b07-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b07-132">-WhatIf</span></span>
<span data-ttu-id="12b07-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12b07-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b07-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12b07-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b07-135">CommonParameters</span></span>
<span data-ttu-id="12b07-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b07-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12b07-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b07-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12b07-138">INPUTS</span></span>

### <span data-ttu-id="12b07-139">System. String</span><span class="sxs-lookup"><span data-stu-id="12b07-139">System.String</span></span>

### <span data-ttu-id="12b07-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="12b07-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="12b07-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12b07-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="12b07-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12b07-142">OUTPUTS</span></span>

### <span data-ttu-id="12b07-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="12b07-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="12b07-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12b07-144">NOTES</span></span>

## <span data-ttu-id="12b07-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12b07-145">RELATED LINKS</span></span>
