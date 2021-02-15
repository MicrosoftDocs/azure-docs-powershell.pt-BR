---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112124"
---
# <span data-ttu-id="49d82-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="49d82-101">New-AzGallery</span></span>

## <span data-ttu-id="49d82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49d82-102">SYNOPSIS</span></span>
<span data-ttu-id="49d82-103">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="49d82-103">Create a gallery.</span></span>

## <span data-ttu-id="49d82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49d82-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49d82-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="49d82-105">DESCRIPTION</span></span>
<span data-ttu-id="49d82-106">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="49d82-106">Create a gallery.</span></span>

## <span data-ttu-id="49d82-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49d82-107">EXAMPLES</span></span>

### <span data-ttu-id="49d82-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="49d82-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="49d82-109">Criar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="49d82-109">Create a gallery.</span></span>

## <span data-ttu-id="49d82-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49d82-110">PARAMETERS</span></span>

### <span data-ttu-id="49d82-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49d82-111">-AsJob</span></span>
<span data-ttu-id="49d82-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49d82-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49d82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d82-113">-DefaultProfile</span></span>
<span data-ttu-id="49d82-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49d82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49d82-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="49d82-115">-Description</span></span>
<span data-ttu-id="49d82-116">A descrição do recurso da galeria.</span><span class="sxs-lookup"><span data-stu-id="49d82-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="49d82-117">-Local</span><span class="sxs-lookup"><span data-stu-id="49d82-117">-Location</span></span>
<span data-ttu-id="49d82-118">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="49d82-118">Resource location</span></span>

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

### <span data-ttu-id="49d82-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="49d82-119">-Name</span></span>
<span data-ttu-id="49d82-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="49d82-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="49d82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d82-121">-ResourceGroupName</span></span>
<span data-ttu-id="49d82-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49d82-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="49d82-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="49d82-123">-Tag</span></span>
<span data-ttu-id="49d82-124">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="49d82-124">Resource tags</span></span>

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

### <span data-ttu-id="49d82-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="49d82-125">-Confirm</span></span>
<span data-ttu-id="49d82-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49d82-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49d82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d82-127">-WhatIf</span></span>
<span data-ttu-id="49d82-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="49d82-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49d82-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49d82-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49d82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d82-130">CommonParameters</span></span>
<span data-ttu-id="49d82-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d82-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49d82-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d82-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="49d82-133">INPUTS</span></span>

### <span data-ttu-id="49d82-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49d82-134">System.String</span></span>

### <span data-ttu-id="49d82-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="49d82-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49d82-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="49d82-136">OUTPUTS</span></span>

### <span data-ttu-id="49d82-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="49d82-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="49d82-138">Notas</span><span class="sxs-lookup"><span data-stu-id="49d82-138">NOTES</span></span>

## <span data-ttu-id="49d82-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49d82-139">RELATED LINKS</span></span>
