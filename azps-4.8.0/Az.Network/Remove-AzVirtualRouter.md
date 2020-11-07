---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954802"
---
# <span data-ttu-id="594b0-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="594b0-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="594b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="594b0-102">SYNOPSIS</span></span>
<span data-ttu-id="594b0-103">Exclui um VirtualRouter do Azure.</span><span class="sxs-lookup"><span data-stu-id="594b0-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="594b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="594b0-104">SYNTAX</span></span>

### <span data-ttu-id="594b0-105">VirtualRouterNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="594b0-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594b0-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="594b0-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594b0-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="594b0-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="594b0-108">DESCRIPTION</span></span>
<span data-ttu-id="594b0-109">O cmdlet **Remove-AzVirtualRouter** exclui um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="594b0-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="594b0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="594b0-110">EXAMPLES</span></span>

### <span data-ttu-id="594b0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="594b0-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="594b0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="594b0-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="594b0-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="594b0-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="594b0-114">OS</span><span class="sxs-lookup"><span data-stu-id="594b0-114">PARAMETERS</span></span>

### <span data-ttu-id="594b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="594b0-115">-AsJob</span></span>
<span data-ttu-id="594b0-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="594b0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="594b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594b0-117">-DefaultProfile</span></span>
<span data-ttu-id="594b0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="594b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594b0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="594b0-119">-Force</span></span>
<span data-ttu-id="594b0-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="594b0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="594b0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="594b0-121">-InputObject</span></span>
<span data-ttu-id="594b0-122">O objeto de entrada do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="594b0-122">The virtual router input object.</span></span>

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

### <span data-ttu-id="594b0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="594b0-123">-PassThru</span></span>
<span data-ttu-id="594b0-124">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="594b0-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="594b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="594b0-126">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="594b0-126">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="594b0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="594b0-127">-ResourceId</span></span>
<span data-ttu-id="594b0-128">A ID de recurso do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="594b0-128">The virtual router resource Id.</span></span>

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

### <span data-ttu-id="594b0-129">-Roteadorname</span><span class="sxs-lookup"><span data-stu-id="594b0-129">-RouterName</span></span>
<span data-ttu-id="594b0-130">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="594b0-130">The name of the virtual router.</span></span>

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

### <span data-ttu-id="594b0-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="594b0-131">-Confirm</span></span>
<span data-ttu-id="594b0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="594b0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594b0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594b0-133">-WhatIf</span></span>
<span data-ttu-id="594b0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="594b0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594b0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="594b0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594b0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594b0-136">CommonParameters</span></span>
<span data-ttu-id="594b0-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594b0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594b0-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="594b0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594b0-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="594b0-139">INPUTS</span></span>

### <span data-ttu-id="594b0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="594b0-140">System.String</span></span>

### <span data-ttu-id="594b0-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="594b0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="594b0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="594b0-142">OUTPUTS</span></span>

### <span data-ttu-id="594b0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="594b0-143">System.Boolean</span></span>

## <span data-ttu-id="594b0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="594b0-144">NOTES</span></span>

## <span data-ttu-id="594b0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="594b0-145">RELATED LINKS</span></span>
