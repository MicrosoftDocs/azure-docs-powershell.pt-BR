---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2cafba2d579a37db45f12c5e3dd1746f799bfe21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885986"
---
# <span data-ttu-id="1176c-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1176c-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1176c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1176c-102">SYNOPSIS</span></span>
<span data-ttu-id="1176c-103">Obtém uma configuração de IP front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1176c-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="1176c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1176c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1176c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1176c-105">DESCRIPTION</span></span>
<span data-ttu-id="1176c-106">O cmdlet **Get-AzLoadBalancerFrontendIpConfig** obtém uma configuração de IP front-end ou uma lista de configurações de IP front-end em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1176c-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="1176c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1176c-107">EXAMPLES</span></span>

### <span data-ttu-id="1176c-108">Exemplo 1: obter uma configuração de IP front-end em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="1176c-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="1176c-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="1176c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="1176c-110">O segundo comando obtém a configuração de IP front-end associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1176c-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="1176c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1176c-111">PARAMETERS</span></span>

### <span data-ttu-id="1176c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1176c-112">-DefaultProfile</span></span>
<span data-ttu-id="1176c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1176c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1176c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1176c-114">-LoadBalancer</span></span>
<span data-ttu-id="1176c-115">Especifica o balanceador de carga associado à configuração de IP front-end a ser obter.</span><span class="sxs-lookup"><span data-stu-id="1176c-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="1176c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1176c-116">-Name</span></span>
<span data-ttu-id="1176c-117">Especifica o nome do balanceador de carga que contém a configuração de IP front-end a ser obter.</span><span class="sxs-lookup"><span data-stu-id="1176c-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="1176c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1176c-118">CommonParameters</span></span>
<span data-ttu-id="1176c-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1176c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1176c-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1176c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1176c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1176c-121">INPUTS</span></span>

### <span data-ttu-id="1176c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1176c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1176c-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1176c-123">OUTPUTS</span></span>

### <span data-ttu-id="1176c-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1176c-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="1176c-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="1176c-125">NOTES</span></span>

## <span data-ttu-id="1176c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1176c-126">RELATED LINKS</span></span>

[<span data-ttu-id="1176c-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1176c-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1176c-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1176c-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1176c-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1176c-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1176c-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1176c-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1176c-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1176c-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


