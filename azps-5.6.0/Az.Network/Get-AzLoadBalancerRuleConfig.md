---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892455"
---
# <span data-ttu-id="f5311-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5311-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f5311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5311-102">SYNOPSIS</span></span>
<span data-ttu-id="f5311-103">Obtém a configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f5311-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f5311-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5311-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5311-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5311-105">DESCRIPTION</span></span>
<span data-ttu-id="f5311-106">O cmdlet **Get-AzLoadBalancerRuleConfig obtém** uma ou mais configurações de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f5311-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="f5311-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5311-107">EXAMPLES</span></span>

### <span data-ttu-id="f5311-108">Exemplo 1: Obter a configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f5311-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="f5311-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="f5311-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f5311-110">O segundo comando obtém a configuração de regra associada chamada MyLBrulename do balanceador de carga no $slb.</span><span class="sxs-lookup"><span data-stu-id="f5311-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="f5311-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5311-111">PARAMETERS</span></span>

### <span data-ttu-id="f5311-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5311-112">-DefaultProfile</span></span>
<span data-ttu-id="f5311-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f5311-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5311-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5311-114">-LoadBalancer</span></span>
<span data-ttu-id="f5311-115">Especifica o balanceador de carga associado à configuração de regra a ser obter.</span><span class="sxs-lookup"><span data-stu-id="f5311-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="f5311-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f5311-116">-Name</span></span>
<span data-ttu-id="f5311-117">Especifica o nome da configuração de regra a ser obter.</span><span class="sxs-lookup"><span data-stu-id="f5311-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="f5311-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5311-118">CommonParameters</span></span>
<span data-ttu-id="f5311-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5311-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5311-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5311-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5311-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5311-121">INPUTS</span></span>

### <span data-ttu-id="f5311-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5311-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f5311-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5311-123">OUTPUTS</span></span>

### <span data-ttu-id="f5311-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f5311-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="f5311-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5311-125">NOTES</span></span>

## <span data-ttu-id="f5311-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5311-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5311-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5311-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f5311-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f5311-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f5311-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5311-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f5311-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5311-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


