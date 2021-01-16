---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262464"
---
# <span data-ttu-id="2a497-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a497-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2a497-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a497-102">SYNOPSIS</span></span>
<span data-ttu-id="2a497-103">Obtém uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a497-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="2a497-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a497-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a497-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a497-105">DESCRIPTION</span></span>
<span data-ttu-id="2a497-106">O cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** Obtém uma ou mais regras de entrada de NAT (conversão de endereço de rede) em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a497-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="2a497-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a497-107">EXAMPLES</span></span>

### <span data-ttu-id="2a497-108">Exemplo 1: obter uma configuração de regra NAT de entrada</span><span class="sxs-lookup"><span data-stu-id="2a497-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="2a497-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="2a497-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="2a497-110">O segundo comando obtém a regra NAT associada chamada MyInboundNatRule1 do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="2a497-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="2a497-111">OS</span><span class="sxs-lookup"><span data-stu-id="2a497-111">PARAMETERS</span></span>

### <span data-ttu-id="2a497-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a497-112">-DefaultProfile</span></span>
<span data-ttu-id="2a497-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a497-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a497-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="2a497-114">-LoadBalancer</span></span>
<span data-ttu-id="2a497-115">Especifica o balanceador de carga que está associado à configuração de regra NAT de entrada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2a497-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2a497-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a497-116">-Name</span></span>
<span data-ttu-id="2a497-117">Especifica o nome da configuração de regra NAT de entrada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2a497-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2a497-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a497-118">CommonParameters</span></span>
<span data-ttu-id="2a497-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a497-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a497-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a497-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a497-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a497-121">INPUTS</span></span>

### <span data-ttu-id="2a497-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a497-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2a497-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a497-123">OUTPUTS</span></span>

### <span data-ttu-id="2a497-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2a497-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="2a497-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a497-125">NOTES</span></span>

## <span data-ttu-id="2a497-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a497-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a497-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a497-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2a497-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a497-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2a497-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a497-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2a497-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a497-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


