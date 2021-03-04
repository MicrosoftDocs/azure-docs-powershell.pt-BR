---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 783eb017f336cd587f51f286cad296c267e6b68c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891335"
---
# <span data-ttu-id="b8901-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8901-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="b8901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8901-102">SYNOPSIS</span></span>
<span data-ttu-id="b8901-103">Cria um pool de endereços back-end em um loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b8901-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="b8901-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8901-104">SYNTAX</span></span>

### <span data-ttu-id="b8901-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8901-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8901-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8901-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8901-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8901-107">DESCRIPTION</span></span>
<span data-ttu-id="b8901-108">Cria um pool de endereços back-end em um loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b8901-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="b8901-109">Permite especificar uma matriz de PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="b8901-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="b8901-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8901-110">EXAMPLES</span></span>

### <span data-ttu-id="b8901-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8901-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="b8901-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8901-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="b8901-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b8901-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="b8901-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b8901-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="b8901-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8901-115">PARAMETERS</span></span>

### <span data-ttu-id="b8901-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8901-116">-DefaultProfile</span></span>
<span data-ttu-id="b8901-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8901-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8901-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8901-118">-LoadBalancer</span></span>
<span data-ttu-id="b8901-119">O recurso balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b8901-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="b8901-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b8901-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="b8901-121">Os endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="b8901-121">The backend addresses.</span></span>

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

### <span data-ttu-id="b8901-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b8901-122">-LoadBalancerName</span></span>
<span data-ttu-id="b8901-123">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b8901-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="b8901-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b8901-124">-Name</span></span>
<span data-ttu-id="b8901-125">O nome do pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="b8901-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="b8901-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8901-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8901-127">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b8901-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="b8901-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8901-128">-Confirm</span></span>
<span data-ttu-id="b8901-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8901-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8901-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8901-130">-WhatIf</span></span>
<span data-ttu-id="b8901-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8901-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8901-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8901-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8901-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8901-133">CommonParameters</span></span>
<span data-ttu-id="b8901-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8901-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8901-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8901-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8901-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8901-136">INPUTS</span></span>

### <span data-ttu-id="b8901-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8901-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b8901-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8901-138">OUTPUTS</span></span>

### <span data-ttu-id="b8901-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b8901-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b8901-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8901-140">NOTES</span></span>

## <span data-ttu-id="b8901-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8901-141">RELATED LINKS</span></span>
