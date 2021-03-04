---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 6e12cc4bb296a1c523547aebc44c6992dd2b687e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890765"
---
# <span data-ttu-id="a99b1-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a99b1-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="a99b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a99b1-103">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a99b1-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="a99b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a99b1-104">SYNTAX</span></span>

### <span data-ttu-id="a99b1-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b1-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99b1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b1-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a99b1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99b1-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b1-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99b1-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a99b1-109">DESCRIPTION</span></span>
<span data-ttu-id="a99b1-110">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a99b1-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="a99b1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a99b1-111">EXAMPLES</span></span>

### <span data-ttu-id="a99b1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a99b1-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="a99b1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a99b1-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="a99b1-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a99b1-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="a99b1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a99b1-115">PARAMETERS</span></span>

### <span data-ttu-id="a99b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99b1-116">-DefaultProfile</span></span>
<span data-ttu-id="a99b1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a99b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a99b1-118">-InputObject</span></span>
<span data-ttu-id="a99b1-119">O pool de endereços back-end a ser removido</span><span class="sxs-lookup"><span data-stu-id="a99b1-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99b1-120">-LoadBalancer</span></span>
<span data-ttu-id="a99b1-121">O recurso balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a99b1-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a99b1-122">-LoadBalancerName</span></span>
<span data-ttu-id="a99b1-123">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a99b1-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a99b1-124">-Name</span></span>
<span data-ttu-id="a99b1-125">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a99b1-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a99b1-126">-PassThru</span></span>
<span data-ttu-id="a99b1-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a99b1-127">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="a99b1-129">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a99b1-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a99b1-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a99b1-131">-Confirm</span></span>
<span data-ttu-id="a99b1-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a99b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99b1-133">-WhatIf</span></span>
<span data-ttu-id="a99b1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a99b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99b1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a99b1-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99b1-136">CommonParameters</span></span>
<span data-ttu-id="a99b1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99b1-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a99b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99b1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a99b1-139">INPUTS</span></span>

### <span data-ttu-id="a99b1-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a99b1-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a99b1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a99b1-141">System.String</span></span>

## <span data-ttu-id="a99b1-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a99b1-142">OUTPUTS</span></span>

### <span data-ttu-id="a99b1-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a99b1-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a99b1-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a99b1-144">NOTES</span></span>

## <span data-ttu-id="a99b1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a99b1-145">RELATED LINKS</span></span>
