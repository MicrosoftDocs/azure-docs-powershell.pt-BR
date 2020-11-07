---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9c2341494f1508563523a181532ce98347051ac3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775542"
---
# <span data-ttu-id="b7493-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b7493-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b7493-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7493-102">SYNOPSIS</span></span>
<span data-ttu-id="b7493-103">Obtém uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7493-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b7493-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7493-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7493-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7493-105">DESCRIPTION</span></span>
<span data-ttu-id="b7493-106">O cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** Obtém um único pool de endereços back-end ou uma lista de pools de endereços back-end dentro de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7493-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="b7493-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7493-107">EXAMPLES</span></span>

### <span data-ttu-id="b7493-108">Exemplo 1: obter o pool de endereços back-end</span><span class="sxs-lookup"><span data-stu-id="b7493-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b7493-109">O primeiro comando obtém um balanceador de carga existente chamado MyLoadBalancer no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b7493-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="b7493-110">O segundo comando obtém a configuração de pool de endereços back-end associada chamada BackendAddressPool02 para o balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b7493-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b7493-111">OS</span><span class="sxs-lookup"><span data-stu-id="b7493-111">PARAMETERS</span></span>

### <span data-ttu-id="b7493-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7493-112">-DefaultProfile</span></span>
<span data-ttu-id="b7493-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7493-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7493-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b7493-114">-LoadBalancer</span></span>
<span data-ttu-id="b7493-115">Especifica o balanceador de carga que está associado ao pool de endereços back-end para obter.</span><span class="sxs-lookup"><span data-stu-id="b7493-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7493-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7493-116">-Name</span></span>
<span data-ttu-id="b7493-117">Especifica o nome do balanceador de carga que contém o pool de endereços de back-end a obter.</span><span class="sxs-lookup"><span data-stu-id="b7493-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="b7493-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7493-118">CommonParameters</span></span>
<span data-ttu-id="b7493-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7493-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7493-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7493-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7493-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7493-121">INPUTS</span></span>

### <span data-ttu-id="b7493-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7493-122">PSLoadBalancer</span></span>
<span data-ttu-id="b7493-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b7493-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b7493-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7493-124">OUTPUTS</span></span>

### <span data-ttu-id="b7493-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7493-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b7493-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7493-126">NOTES</span></span>

## <span data-ttu-id="b7493-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7493-127">RELATED LINKS</span></span>

[<span data-ttu-id="b7493-128">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b7493-128">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b7493-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7493-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b7493-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b7493-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b7493-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b7493-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

