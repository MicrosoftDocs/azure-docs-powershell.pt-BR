---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: aff2fccde6fc43b9153d8da421f34a6038688fd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772278"
---
# <span data-ttu-id="00c5d-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c5d-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="00c5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="00c5d-103">Remove uma configuração de regra de saída de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="00c5d-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="00c5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00c5d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00c5d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="00c5d-106">O cmdlet **Remove-AzLoadBalancerOutboundRuleConfig** remove uma configuração de regra de saída de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="00c5d-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="00c5d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="00c5d-108">Exemplo 1: excluir uma regra de saída de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="00c5d-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="00c5d-109">O primeiro comando obtém o balanceador de carga associado à configuração de regra de saída que você deseja remover e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="00c5d-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="00c5d-110">O segundo comando Remove a configuração de regra de saída associada do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="00c5d-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="00c5d-111">O terceiro comando atualiza o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="00c5d-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="00c5d-112">OS</span><span class="sxs-lookup"><span data-stu-id="00c5d-112">PARAMETERS</span></span>

### <span data-ttu-id="00c5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c5d-113">-DefaultProfile</span></span>
<span data-ttu-id="00c5d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00c5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00c5d-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="00c5d-115">-LoadBalancer</span></span>
<span data-ttu-id="00c5d-116">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="00c5d-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="00c5d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c5d-117">-Name</span></span>
<span data-ttu-id="00c5d-118">O nome da regra de saída</span><span class="sxs-lookup"><span data-stu-id="00c5d-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c5d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00c5d-119">-Confirm</span></span>
<span data-ttu-id="00c5d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00c5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00c5d-121">-WhatIf</span></span>
<span data-ttu-id="00c5d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00c5d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00c5d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00c5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00c5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c5d-124">CommonParameters</span></span>
<span data-ttu-id="00c5d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c5d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c5d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c5d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00c5d-127">INPUTS</span></span>

### <span data-ttu-id="00c5d-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00c5d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00c5d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00c5d-129">OUTPUTS</span></span>

### <span data-ttu-id="00c5d-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00c5d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00c5d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00c5d-131">NOTES</span></span>

## <span data-ttu-id="00c5d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00c5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="00c5d-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c5d-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="00c5d-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c5d-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="00c5d-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c5d-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="00c5d-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c5d-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)