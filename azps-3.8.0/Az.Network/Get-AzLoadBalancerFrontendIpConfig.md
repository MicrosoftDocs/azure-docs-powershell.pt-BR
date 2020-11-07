---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943337"
---
# <span data-ttu-id="f2e4a-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2e4a-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f2e4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e4a-103">Obtém uma configuração de IP de front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="f2e4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2e4a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e4a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e4a-106">O cmdlet **Get-AzLoadBalancerFrontendIpConfig** Obtém uma configuração de IP de front-end ou uma lista de configurações de IP front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="f2e4a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e4a-108">Exemplo 1: obter uma configuração de IP front-end em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f2e4a-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="f2e4a-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f2e4a-110">O segundo comando obtém a configuração de IP de front-end associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="f2e4a-111">OS</span><span class="sxs-lookup"><span data-stu-id="f2e4a-111">PARAMETERS</span></span>

### <span data-ttu-id="f2e4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e4a-112">-DefaultProfile</span></span>
<span data-ttu-id="f2e4a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e4a-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f2e4a-114">-LoadBalancer</span></span>
<span data-ttu-id="f2e4a-115">Especifica o balanceador de carga que está associado à configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="f2e4a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2e4a-116">-Name</span></span>
<span data-ttu-id="f2e4a-117">Especifica o nome do balanceador de carga que contém a configuração de IP de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="f2e4a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e4a-118">CommonParameters</span></span>
<span data-ttu-id="f2e4a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e4a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e4a-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2e4a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e4a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2e4a-121">INPUTS</span></span>

### <span data-ttu-id="f2e4a-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2e4a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2e4a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2e4a-123">OUTPUTS</span></span>

### <span data-ttu-id="f2e4a-124">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2e4a-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="f2e4a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2e4a-125">NOTES</span></span>

## <span data-ttu-id="f2e4a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2e4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2e4a-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2e4a-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f2e4a-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2e4a-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f2e4a-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2e4a-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f2e4a-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2e4a-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f2e4a-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2e4a-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


