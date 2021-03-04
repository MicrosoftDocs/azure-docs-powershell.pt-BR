---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b32f36e55df3c00ee7539c082f863be563b874b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891132"
---
# <span data-ttu-id="b782a-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b782a-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b782a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b782a-102">SYNOPSIS</span></span>
<span data-ttu-id="b782a-103">Remove uma configuração de regra NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b782a-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="b782a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b782a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b782a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b782a-105">DESCRIPTION</span></span>
<span data-ttu-id="b782a-106">O cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** remove uma configuração de regra nat (conversão de endereço de rede de entrada) de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="b782a-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="b782a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b782a-107">EXAMPLES</span></span>

### <span data-ttu-id="b782a-108">1: Excluir uma regra NAT de entrada de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="b782a-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b782a-109">O primeiro comando carrega um balanceador de carga já existente chamado "mylb" e o armazena na variável $load balanceador.</span><span class="sxs-lookup"><span data-stu-id="b782a-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="b782a-110">O segundo comando remove a regra NAT de entrada associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b782a-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="b782a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b782a-111">PARAMETERS</span></span>

### <span data-ttu-id="b782a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b782a-112">-DefaultProfile</span></span>
<span data-ttu-id="b782a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b782a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b782a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b782a-114">-LoadBalancer</span></span>
<span data-ttu-id="b782a-115">Especifica o **objeto LoadBalancer** que contém a configuração de regra NAT de entrada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b782a-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b782a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b782a-116">-Name</span></span>
<span data-ttu-id="b782a-117">Especifica o nome da configuração de regra NAT de entrada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b782a-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b782a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b782a-118">-Confirm</span></span>
<span data-ttu-id="b782a-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b782a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b782a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b782a-120">-WhatIf</span></span>
<span data-ttu-id="b782a-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b782a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b782a-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b782a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b782a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b782a-123">CommonParameters</span></span>
<span data-ttu-id="b782a-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b782a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b782a-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b782a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b782a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b782a-126">INPUTS</span></span>

### <span data-ttu-id="b782a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b782a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b782a-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b782a-128">OUTPUTS</span></span>

### <span data-ttu-id="b782a-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b782a-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b782a-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="b782a-130">NOTES</span></span>

## <span data-ttu-id="b782a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b782a-131">RELATED LINKS</span></span>

[<span data-ttu-id="b782a-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b782a-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b782a-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b782a-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b782a-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b782a-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b782a-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b782a-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


