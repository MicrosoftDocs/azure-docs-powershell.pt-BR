---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111630"
---
# <span data-ttu-id="a77b7-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a77b7-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="a77b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a77b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a77b7-103">Cria um pool de endereços back-end em um loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a77b7-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="a77b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a77b7-104">SYNTAX</span></span>

### <span data-ttu-id="a77b7-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a77b7-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77b7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a77b7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a77b7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a77b7-107">DESCRIPTION</span></span>
<span data-ttu-id="a77b7-108">Cria um pool de endereços back-end em um loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a77b7-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="a77b7-109">Permite especificar uma matriz de PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="a77b7-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="a77b7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a77b7-110">EXAMPLES</span></span>

### <span data-ttu-id="a77b7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a77b7-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="a77b7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a77b7-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="a77b7-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a77b7-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="a77b7-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a77b7-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="a77b7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a77b7-115">PARAMETERS</span></span>

### <span data-ttu-id="a77b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77b7-116">-DefaultProfile</span></span>
<span data-ttu-id="a77b7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a77b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a77b7-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a77b7-118">-LoadBalancer</span></span>
<span data-ttu-id="a77b7-119">O recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a77b7-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a77b7-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a77b7-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="a77b7-121">Os endereços de back-end.</span><span class="sxs-lookup"><span data-stu-id="a77b7-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b7-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a77b7-122">-LoadBalancerName</span></span>
<span data-ttu-id="a77b7-123">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a77b7-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a77b7-124">-Name</span></span>
<span data-ttu-id="a77b7-125">O nome do pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="a77b7-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="a77b7-127">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a77b7-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77b7-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a77b7-128">-Confirm</span></span>
<span data-ttu-id="a77b7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a77b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a77b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77b7-130">-WhatIf</span></span>
<span data-ttu-id="a77b7-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a77b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a77b7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a77b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a77b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77b7-133">CommonParameters</span></span>
<span data-ttu-id="a77b7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77b7-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a77b7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77b7-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a77b7-136">INPUTS</span></span>

### <span data-ttu-id="a77b7-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a77b7-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a77b7-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="a77b7-138">OUTPUTS</span></span>

### <span data-ttu-id="a77b7-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a77b7-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a77b7-140">Notas</span><span class="sxs-lookup"><span data-stu-id="a77b7-140">NOTES</span></span>

## <span data-ttu-id="a77b7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a77b7-141">RELATED LINKS</span></span>
