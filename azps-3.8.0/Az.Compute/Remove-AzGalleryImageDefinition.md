---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784929"
---
# <span data-ttu-id="a6cdc-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cdc-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="a6cdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cdc-103">Excluir uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="a6cdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6cdc-104">SYNTAX</span></span>

### <span data-ttu-id="a6cdc-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6cdc-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6cdc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a6cdc-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6cdc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a6cdc-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6cdc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="a6cdc-109">Excluir uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="a6cdc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="a6cdc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6cdc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="a6cdc-112">Remover a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="a6cdc-113">OS</span><span class="sxs-lookup"><span data-stu-id="a6cdc-113">PARAMETERS</span></span>

### <span data-ttu-id="a6cdc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6cdc-114">-AsJob</span></span>
<span data-ttu-id="a6cdc-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a6cdc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6cdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6cdc-116">-DefaultProfile</span></span>
<span data-ttu-id="a6cdc-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6cdc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a6cdc-118">-Force</span></span>
<span data-ttu-id="a6cdc-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6cdc-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="a6cdc-120">-GalleryName</span></span>
<span data-ttu-id="a6cdc-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cdc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6cdc-122">-InputObject</span></span>
<span data-ttu-id="a6cdc-123">O objeto de definição de imagem da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="a6cdc-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cdc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6cdc-124">-Name</span></span>
<span data-ttu-id="a6cdc-125">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cdc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6cdc-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6cdc-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6cdc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6cdc-128">-ResourceId</span></span>
<span data-ttu-id="a6cdc-129">A ID do recurso da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="a6cdc-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="a6cdc-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6cdc-130">-Confirm</span></span>
<span data-ttu-id="a6cdc-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6cdc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6cdc-132">-WhatIf</span></span>
<span data-ttu-id="a6cdc-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6cdc-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6cdc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cdc-135">CommonParameters</span></span>
<span data-ttu-id="a6cdc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cdc-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6cdc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cdc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6cdc-138">INPUTS</span></span>

### <span data-ttu-id="a6cdc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a6cdc-139">System.String</span></span>

### <span data-ttu-id="a6cdc-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="a6cdc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="a6cdc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6cdc-141">OUTPUTS</span></span>

### <span data-ttu-id="a6cdc-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a6cdc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a6cdc-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6cdc-143">NOTES</span></span>

## <span data-ttu-id="a6cdc-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6cdc-144">RELATED LINKS</span></span>
