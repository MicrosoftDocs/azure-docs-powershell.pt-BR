---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434280"
---
# <span data-ttu-id="ae0ce-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="ae0ce-101">Remove-AzGallery</span></span>

## <span data-ttu-id="ae0ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0ce-103">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-103">Delete a gallery.</span></span>

## <span data-ttu-id="ae0ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae0ce-104">SYNTAX</span></span>

### <span data-ttu-id="ae0ce-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae0ce-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae0ce-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ae0ce-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae0ce-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ae0ce-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae0ce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae0ce-108">DESCRIPTION</span></span>
<span data-ttu-id="ae0ce-109">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-109">Delete a gallery.</span></span>

## <span data-ttu-id="ae0ce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae0ce-110">EXAMPLES</span></span>

### <span data-ttu-id="ae0ce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae0ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="ae0ce-112">Excluir a Galeria fornecida.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-112">Delete the given gallery.</span></span>

## <span data-ttu-id="ae0ce-113">OS</span><span class="sxs-lookup"><span data-stu-id="ae0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="ae0ce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae0ce-114">-AsJob</span></span>
<span data-ttu-id="ae0ce-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae0ce-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae0ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0ce-116">-DefaultProfile</span></span>
<span data-ttu-id="ae0ce-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae0ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ae0ce-118">-Force</span></span>
<span data-ttu-id="ae0ce-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae0ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae0ce-120">-InputObject</span></span>
<span data-ttu-id="ae0ce-121">O objeto da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="ae0ce-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="ae0ce-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae0ce-122">-Name</span></span>
<span data-ttu-id="ae0ce-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="ae0ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae0ce-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae0ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae0ce-126">-ResourceId</span></span>
<span data-ttu-id="ae0ce-127">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="ae0ce-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="ae0ce-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae0ce-128">-Confirm</span></span>
<span data-ttu-id="ae0ce-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0ce-130">-WhatIf</span></span>
<span data-ttu-id="ae0ce-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0ce-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0ce-133">CommonParameters</span></span>
<span data-ttu-id="ae0ce-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae0ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0ce-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae0ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0ce-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae0ce-136">INPUTS</span></span>

### <span data-ttu-id="ae0ce-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ae0ce-137">System.String</span></span>

### <span data-ttu-id="ae0ce-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ae0ce-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ae0ce-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae0ce-139">OUTPUTS</span></span>

### <span data-ttu-id="ae0ce-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ae0ce-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ae0ce-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae0ce-141">NOTES</span></span>

## <span data-ttu-id="ae0ce-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae0ce-142">RELATED LINKS</span></span>
