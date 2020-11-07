---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954864"
---
# <span data-ttu-id="a327c-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a327c-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a327c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a327c-102">SYNOPSIS</span></span>
<span data-ttu-id="a327c-103">Obtém a configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a327c-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a327c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a327c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a327c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a327c-105">DESCRIPTION</span></span>
<span data-ttu-id="a327c-106">O cmdlet **Get-AzLoadBalancerRuleConfig** Obtém uma ou mais configurações de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a327c-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="a327c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a327c-107">EXAMPLES</span></span>

### <span data-ttu-id="a327c-108">Exemplo 1: obter a configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a327c-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="a327c-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="a327c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a327c-110">O segundo comando obtém a configuração de regra associada nomeada MyLBrulename do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="a327c-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="a327c-111">OS</span><span class="sxs-lookup"><span data-stu-id="a327c-111">PARAMETERS</span></span>

### <span data-ttu-id="a327c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a327c-112">-DefaultProfile</span></span>
<span data-ttu-id="a327c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a327c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a327c-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="a327c-114">-LoadBalancer</span></span>
<span data-ttu-id="a327c-115">Especifica o balanceador de carga associado à configuração de regra a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="a327c-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="a327c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a327c-116">-Name</span></span>
<span data-ttu-id="a327c-117">Especifica o nome da configuração da regra a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="a327c-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="a327c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a327c-118">CommonParameters</span></span>
<span data-ttu-id="a327c-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a327c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a327c-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a327c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a327c-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a327c-121">INPUTS</span></span>

### <span data-ttu-id="a327c-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a327c-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a327c-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a327c-123">OUTPUTS</span></span>

### <span data-ttu-id="a327c-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a327c-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="a327c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a327c-125">NOTES</span></span>

## <span data-ttu-id="a327c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a327c-126">RELATED LINKS</span></span>

[<span data-ttu-id="a327c-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a327c-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a327c-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a327c-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a327c-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a327c-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a327c-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a327c-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


