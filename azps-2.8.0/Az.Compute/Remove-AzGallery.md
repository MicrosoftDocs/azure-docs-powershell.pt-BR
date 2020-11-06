---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: ac098616d2ee92b4d6910034735824289b971f5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597329"
---
# <span data-ttu-id="38f9c-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="38f9c-101">Remove-AzGallery</span></span>

## <span data-ttu-id="38f9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="38f9c-103">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="38f9c-103">Delete a gallery.</span></span>

## <span data-ttu-id="38f9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f9c-104">SYNTAX</span></span>

### <span data-ttu-id="38f9c-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="38f9c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f9c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="38f9c-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f9c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="38f9c-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f9c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="38f9c-109">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="38f9c-109">Delete a gallery.</span></span>

## <span data-ttu-id="38f9c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38f9c-110">EXAMPLES</span></span>

### <span data-ttu-id="38f9c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38f9c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="38f9c-112">Excluir a Galeria fornecida.</span><span class="sxs-lookup"><span data-stu-id="38f9c-112">Delete the given gallery.</span></span>

## <span data-ttu-id="38f9c-113">OS</span><span class="sxs-lookup"><span data-stu-id="38f9c-113">PARAMETERS</span></span>

### <span data-ttu-id="38f9c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38f9c-114">-AsJob</span></span>
<span data-ttu-id="38f9c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38f9c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38f9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f9c-116">-DefaultProfile</span></span>
<span data-ttu-id="38f9c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38f9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f9c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38f9c-118">-Force</span></span>
<span data-ttu-id="38f9c-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="38f9c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38f9c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f9c-120">-InputObject</span></span>
<span data-ttu-id="38f9c-121">O objeto da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="38f9c-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="38f9c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="38f9c-122">-Name</span></span>
<span data-ttu-id="38f9c-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="38f9c-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="38f9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="38f9c-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38f9c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="38f9c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38f9c-126">-ResourceId</span></span>
<span data-ttu-id="38f9c-127">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="38f9c-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="38f9c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38f9c-128">-Confirm</span></span>
<span data-ttu-id="38f9c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f9c-130">-WhatIf</span></span>
<span data-ttu-id="38f9c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38f9c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f9c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38f9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f9c-133">CommonParameters</span></span>
<span data-ttu-id="38f9c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f9c-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38f9c-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f9c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38f9c-136">INPUTS</span></span>

### <span data-ttu-id="38f9c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="38f9c-137">System.String</span></span>

### <span data-ttu-id="38f9c-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="38f9c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="38f9c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38f9c-139">OUTPUTS</span></span>

### <span data-ttu-id="38f9c-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="38f9c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="38f9c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38f9c-141">NOTES</span></span>

## <span data-ttu-id="38f9c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38f9c-142">RELATED LINKS</span></span>
