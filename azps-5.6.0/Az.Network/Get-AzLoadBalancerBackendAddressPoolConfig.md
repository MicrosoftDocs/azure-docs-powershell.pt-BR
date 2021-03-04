---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a337446238807f3a6408d0c9b68034e4a245eb48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885987"
---
# <span data-ttu-id="b2e3d-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2e3d-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b2e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e3d-103">Obtém uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b2e3d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2e3d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e3d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e3d-106">O cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** obtém um único pool de endereços back-end ou uma lista de pools de endereços back-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="b2e3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e3d-108">Exemplo 1: Obter o pool de endereços back-end</span><span class="sxs-lookup"><span data-stu-id="b2e3d-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b2e3d-109">O primeiro comando obtém um balanceador de carga existente chamado MyLoadBalancer no grupo de recursos chamado MyResourceGroup e o armazena na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="b2e3d-110">O segundo comando obtém a configuração de pool de endereços back-end associado chamada BackendAddressPool02 para o balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b2e3d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-111">PARAMETERS</span></span>

### <span data-ttu-id="b2e3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e3d-112">-DefaultProfile</span></span>
<span data-ttu-id="b2e3d-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e3d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2e3d-114">-LoadBalancer</span></span>
<span data-ttu-id="b2e3d-115">Especifica o balanceador de carga associado ao pool de endereços back-end a ser definido.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e3d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e3d-116">-Name</span></span>
<span data-ttu-id="b2e3d-117">Especifica o nome do balanceador de carga que contém o pool de endereços back-end a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e3d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e3d-118">CommonParameters</span></span>
<span data-ttu-id="b2e3d-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e3d-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2e3d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e3d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-121">INPUTS</span></span>

### <span data-ttu-id="b2e3d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2e3d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b2e3d-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-123">OUTPUTS</span></span>

### <span data-ttu-id="b2e3d-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b2e3d-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b2e3d-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2e3d-125">NOTES</span></span>

## <span data-ttu-id="b2e3d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2e3d-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2e3d-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2e3d-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b2e3d-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2e3d-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b2e3d-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2e3d-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b2e3d-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2e3d-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


