---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110484"
---
# <span data-ttu-id="b39b5-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b39b5-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="b39b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b39b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b39b5-103">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="b39b5-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="b39b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b39b5-104">SYNTAX</span></span>

### <span data-ttu-id="b39b5-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b39b5-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b39b5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b39b5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b39b5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b39b5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b39b5-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b39b5-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b39b5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b39b5-109">DESCRIPTION</span></span>
<span data-ttu-id="b39b5-110">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="b39b5-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="b39b5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b39b5-111">EXAMPLES</span></span>

### <span data-ttu-id="b39b5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b39b5-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="b39b5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b39b5-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="b39b5-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b39b5-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="b39b5-115">OS</span><span class="sxs-lookup"><span data-stu-id="b39b5-115">PARAMETERS</span></span>

### <span data-ttu-id="b39b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39b5-116">-DefaultProfile</span></span>
<span data-ttu-id="b39b5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b39b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b39b5-118">-InputObject</span></span>
<span data-ttu-id="b39b5-119">O pool de endereços de back-end a ser removido</span><span class="sxs-lookup"><span data-stu-id="b39b5-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="b39b5-120">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b39b5-120">-LoadBalancer</span></span>
<span data-ttu-id="b39b5-121">O recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b39b5-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="b39b5-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b39b5-122">-LoadBalancerName</span></span>
<span data-ttu-id="b39b5-123">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b39b5-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="b39b5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b39b5-124">-Name</span></span>
<span data-ttu-id="b39b5-125">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b39b5-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="b39b5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b39b5-126">-PassThru</span></span>
<span data-ttu-id="b39b5-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b39b5-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b39b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b39b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="b39b5-129">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b39b5-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="b39b5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b39b5-130">-ResourceId</span></span>

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

### <span data-ttu-id="b39b5-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b39b5-131">-Confirm</span></span>
<span data-ttu-id="b39b5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b39b5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39b5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39b5-133">-WhatIf</span></span>
<span data-ttu-id="b39b5-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b39b5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b39b5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b39b5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39b5-136">CommonParameters</span></span>
<span data-ttu-id="b39b5-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39b5-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b39b5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39b5-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b39b5-139">INPUTS</span></span>

### <span data-ttu-id="b39b5-140">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b39b5-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b39b5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b39b5-141">System.String</span></span>

## <span data-ttu-id="b39b5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b39b5-142">OUTPUTS</span></span>

### <span data-ttu-id="b39b5-143">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b39b5-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b39b5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b39b5-144">NOTES</span></span>

## <span data-ttu-id="b39b5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b39b5-145">RELATED LINKS</span></span>
