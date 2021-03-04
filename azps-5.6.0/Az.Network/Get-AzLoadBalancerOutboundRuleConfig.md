---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892458"
---
# <span data-ttu-id="ef136-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef136-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="ef136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef136-102">SYNOPSIS</span></span>
<span data-ttu-id="ef136-103">Obtém uma configuração de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ef136-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="ef136-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef136-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef136-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef136-105">DESCRIPTION</span></span>
<span data-ttu-id="ef136-106">O cmdlet **Get-AzLoadBalancerOutboundRuleConfig** obtém uma configuração de regra de saída ou uma lista de configurações de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ef136-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="ef136-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef136-107">EXAMPLES</span></span>

### <span data-ttu-id="ef136-108">Exemplo 1: Obter uma configuração de regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ef136-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="ef136-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="ef136-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ef136-110">O segundo comando obtém a configuração de regra de saída chamada MyRule associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ef136-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="ef136-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef136-111">PARAMETERS</span></span>

### <span data-ttu-id="ef136-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef136-112">-DefaultProfile</span></span>
<span data-ttu-id="ef136-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef136-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef136-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef136-114">-LoadBalancer</span></span>
<span data-ttu-id="ef136-115">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ef136-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="ef136-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef136-116">-Name</span></span>
<span data-ttu-id="ef136-117">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="ef136-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="ef136-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef136-118">CommonParameters</span></span>
<span data-ttu-id="ef136-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef136-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef136-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef136-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef136-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef136-121">INPUTS</span></span>

### <span data-ttu-id="ef136-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ef136-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ef136-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef136-123">OUTPUTS</span></span>

### <span data-ttu-id="ef136-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="ef136-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="ef136-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef136-125">NOTES</span></span>

## <span data-ttu-id="ef136-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef136-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef136-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef136-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef136-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef136-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef136-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef136-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="ef136-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef136-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
