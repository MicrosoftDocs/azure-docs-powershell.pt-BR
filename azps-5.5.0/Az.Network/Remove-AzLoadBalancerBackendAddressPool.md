---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117347"
---
# <span data-ttu-id="04021-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="04021-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="04021-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04021-102">SYNOPSIS</span></span>
<span data-ttu-id="04021-103">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="04021-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="04021-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04021-104">SYNTAX</span></span>

### <span data-ttu-id="04021-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04021-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04021-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04021-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04021-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04021-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04021-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04021-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04021-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="04021-109">DESCRIPTION</span></span>
<span data-ttu-id="04021-110">Remove um pool de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="04021-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="04021-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04021-111">EXAMPLES</span></span>

### <span data-ttu-id="04021-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04021-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="04021-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="04021-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="04021-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="04021-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="04021-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04021-115">PARAMETERS</span></span>

### <span data-ttu-id="04021-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04021-116">-DefaultProfile</span></span>
<span data-ttu-id="04021-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04021-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04021-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04021-118">-InputObject</span></span>
<span data-ttu-id="04021-119">O pool de endereços back-end para remover</span><span class="sxs-lookup"><span data-stu-id="04021-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="04021-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04021-120">-LoadBalancer</span></span>
<span data-ttu-id="04021-121">O recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="04021-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="04021-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="04021-122">-LoadBalancerName</span></span>
<span data-ttu-id="04021-123">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="04021-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="04021-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="04021-124">-Name</span></span>
<span data-ttu-id="04021-125">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="04021-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="04021-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04021-126">-PassThru</span></span>
<span data-ttu-id="04021-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="04021-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="04021-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04021-128">-ResourceGroupName</span></span>
<span data-ttu-id="04021-129">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="04021-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="04021-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04021-130">-ResourceId</span></span>

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

### <span data-ttu-id="04021-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="04021-131">-Confirm</span></span>
<span data-ttu-id="04021-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04021-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04021-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04021-133">-WhatIf</span></span>
<span data-ttu-id="04021-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="04021-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04021-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04021-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04021-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04021-136">CommonParameters</span></span>
<span data-ttu-id="04021-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04021-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04021-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04021-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04021-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="04021-139">INPUTS</span></span>

### <span data-ttu-id="04021-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="04021-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="04021-141">System.String</span><span class="sxs-lookup"><span data-stu-id="04021-141">System.String</span></span>

## <span data-ttu-id="04021-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="04021-142">OUTPUTS</span></span>

### <span data-ttu-id="04021-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="04021-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="04021-144">Notas</span><span class="sxs-lookup"><span data-stu-id="04021-144">NOTES</span></span>

## <span data-ttu-id="04021-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04021-145">RELATED LINKS</span></span>
