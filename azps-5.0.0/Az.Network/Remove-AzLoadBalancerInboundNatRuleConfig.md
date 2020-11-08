---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116074"
---
# <span data-ttu-id="622c5-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="622c5-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="622c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="622c5-102">SYNOPSIS</span></span>
<span data-ttu-id="622c5-103">Remove uma configuração de regra NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="622c5-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="622c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="622c5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="622c5-105">DESCRIPTION</span></span>
<span data-ttu-id="622c5-106">O cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** remove uma configuração de regra NAT (conversão de endereço de rede) de entrada de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="622c5-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="622c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="622c5-107">EXAMPLES</span></span>

### <span data-ttu-id="622c5-108">1: excluir uma regra NAT de entrada de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="622c5-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="622c5-109">O primeiro comando carrega um balanceador de carga já existente chamado "mylb" e o armazena na variável de balanceador de $load.</span><span class="sxs-lookup"><span data-stu-id="622c5-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="622c5-110">O segundo comando Remove a regra NAT de entrada associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="622c5-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="622c5-111">OS</span><span class="sxs-lookup"><span data-stu-id="622c5-111">PARAMETERS</span></span>

### <span data-ttu-id="622c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622c5-112">-DefaultProfile</span></span>
<span data-ttu-id="622c5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="622c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622c5-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="622c5-114">-LoadBalancer</span></span>
<span data-ttu-id="622c5-115">Especifica o objeto **Loadbalancer** que contém a configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="622c5-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="622c5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="622c5-116">-Name</span></span>
<span data-ttu-id="622c5-117">Especifica o nome da configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="622c5-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="622c5-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="622c5-118">-Confirm</span></span>
<span data-ttu-id="622c5-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="622c5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622c5-120">-WhatIf</span></span>
<span data-ttu-id="622c5-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="622c5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="622c5-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="622c5-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622c5-123">CommonParameters</span></span>
<span data-ttu-id="622c5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622c5-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622c5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622c5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="622c5-126">INPUTS</span></span>

### <span data-ttu-id="622c5-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="622c5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="622c5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="622c5-128">OUTPUTS</span></span>

### <span data-ttu-id="622c5-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="622c5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="622c5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="622c5-130">NOTES</span></span>

## <span data-ttu-id="622c5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="622c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="622c5-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="622c5-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="622c5-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="622c5-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="622c5-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="622c5-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="622c5-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="622c5-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


