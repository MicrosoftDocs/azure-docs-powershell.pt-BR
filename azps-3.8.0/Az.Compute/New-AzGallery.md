---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941465"
---
# <span data-ttu-id="15aba-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="15aba-101">New-AzGallery</span></span>

## <span data-ttu-id="15aba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15aba-102">SYNOPSIS</span></span>
<span data-ttu-id="15aba-103">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="15aba-103">Create a gallery.</span></span>

## <span data-ttu-id="15aba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15aba-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15aba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15aba-105">DESCRIPTION</span></span>
<span data-ttu-id="15aba-106">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="15aba-106">Create a gallery.</span></span>

## <span data-ttu-id="15aba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15aba-107">EXAMPLES</span></span>

### <span data-ttu-id="15aba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15aba-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="15aba-109">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="15aba-109">Create a gallery.</span></span>

## <span data-ttu-id="15aba-110">OS</span><span class="sxs-lookup"><span data-stu-id="15aba-110">PARAMETERS</span></span>

### <span data-ttu-id="15aba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15aba-111">-AsJob</span></span>
<span data-ttu-id="15aba-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="15aba-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15aba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15aba-113">-DefaultProfile</span></span>
<span data-ttu-id="15aba-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15aba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15aba-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="15aba-115">-Description</span></span>
<span data-ttu-id="15aba-116">A descrição do recurso de galeria.</span><span class="sxs-lookup"><span data-stu-id="15aba-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="15aba-117">-Local</span><span class="sxs-lookup"><span data-stu-id="15aba-117">-Location</span></span>
<span data-ttu-id="15aba-118">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="15aba-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15aba-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="15aba-119">-Name</span></span>
<span data-ttu-id="15aba-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="15aba-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15aba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15aba-121">-ResourceGroupName</span></span>
<span data-ttu-id="15aba-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15aba-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="15aba-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="15aba-123">-Tag</span></span>
<span data-ttu-id="15aba-124">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="15aba-124">Resource tags</span></span>

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

### <span data-ttu-id="15aba-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15aba-125">-Confirm</span></span>
<span data-ttu-id="15aba-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15aba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15aba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15aba-127">-WhatIf</span></span>
<span data-ttu-id="15aba-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15aba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15aba-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15aba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15aba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15aba-130">CommonParameters</span></span>
<span data-ttu-id="15aba-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15aba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15aba-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15aba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15aba-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15aba-133">INPUTS</span></span>

### <span data-ttu-id="15aba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="15aba-134">System.String</span></span>

### <span data-ttu-id="15aba-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="15aba-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15aba-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15aba-136">OUTPUTS</span></span>

### <span data-ttu-id="15aba-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="15aba-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="15aba-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15aba-138">NOTES</span></span>

## <span data-ttu-id="15aba-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15aba-139">RELATED LINKS</span></span>
