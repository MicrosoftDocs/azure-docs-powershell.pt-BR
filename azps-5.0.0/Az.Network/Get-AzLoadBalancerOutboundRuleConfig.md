---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116225"
---
# <span data-ttu-id="60ddd-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60ddd-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="60ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="60ddd-103">Obtém uma configuração de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="60ddd-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="60ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60ddd-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ddd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="60ddd-106">O cmdlet **Get-AzLoadBalancerOutboundRuleConfig** Obtém uma configuração de regra de saída ou uma lista de configurações de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="60ddd-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="60ddd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="60ddd-108">Exemplo 1: obter uma configuração de regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="60ddd-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="60ddd-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="60ddd-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="60ddd-110">O segundo comando obtém a configuração de regra de saída chamada myrule associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="60ddd-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="60ddd-111">OS</span><span class="sxs-lookup"><span data-stu-id="60ddd-111">PARAMETERS</span></span>

### <span data-ttu-id="60ddd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ddd-112">-DefaultProfile</span></span>
<span data-ttu-id="60ddd-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60ddd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ddd-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="60ddd-114">-LoadBalancer</span></span>
<span data-ttu-id="60ddd-115">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="60ddd-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="60ddd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="60ddd-116">-Name</span></span>
<span data-ttu-id="60ddd-117">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="60ddd-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="60ddd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ddd-118">CommonParameters</span></span>
<span data-ttu-id="60ddd-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ddd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ddd-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60ddd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ddd-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60ddd-121">INPUTS</span></span>

### <span data-ttu-id="60ddd-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="60ddd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="60ddd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60ddd-123">OUTPUTS</span></span>

### <span data-ttu-id="60ddd-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="60ddd-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="60ddd-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60ddd-125">NOTES</span></span>

## <span data-ttu-id="60ddd-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60ddd-126">RELATED LINKS</span></span>

[<span data-ttu-id="60ddd-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60ddd-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="60ddd-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60ddd-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="60ddd-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60ddd-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="60ddd-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60ddd-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
