---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 43ff179aa11c3cf9bf4b22f8b5c938a473a9d8c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601318"
---
# <span data-ttu-id="d99b9-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="d99b9-101">New-AzGallery</span></span>

## <span data-ttu-id="d99b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d99b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d99b9-103">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="d99b9-103">Create a gallery.</span></span>

## <span data-ttu-id="d99b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d99b9-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d99b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d99b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d99b9-106">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="d99b9-106">Create a gallery.</span></span>

## <span data-ttu-id="d99b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d99b9-107">EXAMPLES</span></span>

### <span data-ttu-id="d99b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d99b9-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="d99b9-109">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="d99b9-109">Create a gallery.</span></span>

## <span data-ttu-id="d99b9-110">OS</span><span class="sxs-lookup"><span data-stu-id="d99b9-110">PARAMETERS</span></span>

### <span data-ttu-id="d99b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d99b9-111">-AsJob</span></span>
<span data-ttu-id="d99b9-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d99b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d99b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99b9-113">-DefaultProfile</span></span>
<span data-ttu-id="d99b9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d99b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d99b9-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d99b9-115">-Description</span></span>
<span data-ttu-id="d99b9-116">A descrição do recurso de galeria.</span><span class="sxs-lookup"><span data-stu-id="d99b9-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="d99b9-117">-Local</span><span class="sxs-lookup"><span data-stu-id="d99b9-117">-Location</span></span>
<span data-ttu-id="d99b9-118">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="d99b9-118">Resource location</span></span>

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

### <span data-ttu-id="d99b9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d99b9-119">-Name</span></span>
<span data-ttu-id="d99b9-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="d99b9-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="d99b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d99b9-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d99b9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d99b9-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="d99b9-123">-Tag</span></span>
<span data-ttu-id="d99b9-124">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="d99b9-124">Resource tags</span></span>

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

### <span data-ttu-id="d99b9-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d99b9-125">-Confirm</span></span>
<span data-ttu-id="d99b9-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d99b9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d99b9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d99b9-127">-WhatIf</span></span>
<span data-ttu-id="d99b9-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d99b9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d99b9-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d99b9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d99b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99b9-130">CommonParameters</span></span>
<span data-ttu-id="d99b9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d99b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99b9-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99b9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99b9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d99b9-133">INPUTS</span></span>

### <span data-ttu-id="d99b9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d99b9-134">System.String</span></span>

### <span data-ttu-id="d99b9-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d99b9-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d99b9-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d99b9-136">OUTPUTS</span></span>

### <span data-ttu-id="d99b9-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="d99b9-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="d99b9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d99b9-138">NOTES</span></span>

## <span data-ttu-id="d99b9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d99b9-139">RELATED LINKS</span></span>
