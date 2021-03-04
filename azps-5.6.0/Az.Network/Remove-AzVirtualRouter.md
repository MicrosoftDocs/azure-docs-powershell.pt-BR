---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6def67720ee11a2057267845ef458d0759aec589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892394"
---
# <span data-ttu-id="a0d50-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a0d50-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="a0d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d50-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d50-103">Exclui um Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="a0d50-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="a0d50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a0d50-104">SYNTAX</span></span>

### <span data-ttu-id="a0d50-105">VirtualRouterNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a0d50-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d50-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d50-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d50-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d50-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d50-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a0d50-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d50-109">O cmdlet **Remove-AzVirtualRouter** exclui um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a0d50-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="a0d50-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0d50-110">EXAMPLES</span></span>

### <span data-ttu-id="a0d50-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0d50-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="a0d50-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0d50-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="a0d50-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a0d50-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="a0d50-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a0d50-114">PARAMETERS</span></span>

### <span data-ttu-id="a0d50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0d50-115">-AsJob</span></span>
<span data-ttu-id="a0d50-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a0d50-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0d50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d50-117">-DefaultProfile</span></span>
<span data-ttu-id="a0d50-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d50-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a0d50-119">-Force</span></span>
<span data-ttu-id="a0d50-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="a0d50-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a0d50-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0d50-121">-InputObject</span></span>
<span data-ttu-id="a0d50-122">O objeto de entrada do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d50-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0d50-123">-PassThru</span></span>
<span data-ttu-id="a0d50-124">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a0d50-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a0d50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d50-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0d50-126">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d50-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d50-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0d50-127">-ResourceId</span></span>
<span data-ttu-id="a0d50-128">A ID de recurso do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d50-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d50-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="a0d50-129">-RouterName</span></span>
<span data-ttu-id="a0d50-130">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d50-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d50-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0d50-131">-Confirm</span></span>
<span data-ttu-id="a0d50-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d50-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d50-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d50-133">-WhatIf</span></span>
<span data-ttu-id="a0d50-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0d50-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d50-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0d50-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d50-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d50-136">CommonParameters</span></span>
<span data-ttu-id="a0d50-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d50-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d50-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0d50-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d50-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0d50-139">INPUTS</span></span>

### <span data-ttu-id="a0d50-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a0d50-140">System.String</span></span>

### <span data-ttu-id="a0d50-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a0d50-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a0d50-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a0d50-142">OUTPUTS</span></span>

### <span data-ttu-id="a0d50-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0d50-143">System.Boolean</span></span>

## <span data-ttu-id="a0d50-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a0d50-144">NOTES</span></span>

## <span data-ttu-id="a0d50-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0d50-145">RELATED LINKS</span></span>
