---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885706"
---
# <span data-ttu-id="58747-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58747-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="58747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58747-102">SYNOPSIS</span></span>
<span data-ttu-id="58747-103">Obtém uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="58747-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="58747-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="58747-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58747-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="58747-105">DESCRIPTION</span></span>
<span data-ttu-id="58747-106">O cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** obtém uma ou mais regras de conversão de endereço de rede de entrada (NAT) em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="58747-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="58747-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58747-107">EXAMPLES</span></span>

### <span data-ttu-id="58747-108">Exemplo 1: Obter uma configuração de regra NAT de entrada</span><span class="sxs-lookup"><span data-stu-id="58747-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="58747-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="58747-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="58747-110">O segundo comando obtém a regra NAT associada chamada MyInboundNatRule1 do balanceador de carga no $slb.</span><span class="sxs-lookup"><span data-stu-id="58747-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="58747-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="58747-111">PARAMETERS</span></span>

### <span data-ttu-id="58747-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58747-112">-DefaultProfile</span></span>
<span data-ttu-id="58747-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="58747-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58747-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58747-114">-LoadBalancer</span></span>
<span data-ttu-id="58747-115">Especifica o balanceador de carga associado à configuração de regra NAT de entrada a ser obter.</span><span class="sxs-lookup"><span data-stu-id="58747-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="58747-116">-Name</span><span class="sxs-lookup"><span data-stu-id="58747-116">-Name</span></span>
<span data-ttu-id="58747-117">Especifica o nome da configuração de regra NAT de entrada a ser obter.</span><span class="sxs-lookup"><span data-stu-id="58747-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="58747-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58747-118">CommonParameters</span></span>
<span data-ttu-id="58747-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58747-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58747-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58747-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58747-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58747-121">INPUTS</span></span>

### <span data-ttu-id="58747-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58747-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="58747-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="58747-123">OUTPUTS</span></span>

### <span data-ttu-id="58747-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="58747-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="58747-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="58747-125">NOTES</span></span>

## <span data-ttu-id="58747-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58747-126">RELATED LINKS</span></span>

[<span data-ttu-id="58747-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58747-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="58747-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58747-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="58747-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58747-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="58747-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58747-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


