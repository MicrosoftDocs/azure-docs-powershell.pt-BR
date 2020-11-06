---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431937"
---
# <span data-ttu-id="43239-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="43239-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43239-102">SYNOPSIS</span></span>
<span data-ttu-id="43239-103">Define o estado da meta para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="43239-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43239-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43239-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43239-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43239-105">DESCRIPTION</span></span>
<span data-ttu-id="43239-106">O cmdlet **set-AzureRmLoadBalancer** define o estado da meta para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="43239-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="43239-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43239-107">EXAMPLES</span></span>

### <span data-ttu-id="43239-108">Exemplo 1: modificar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="43239-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="43239-109">O primeiro comando obtém o balanceador de carga chamado NRPLB e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="43239-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="43239-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzureRmLoadBalancerInboundNatRuleConfig, que adiciona uma regra NAT de entrada chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="43239-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="43239-111">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancer** , que atualiza a configuração do balanceador de carga e salva-o.</span><span class="sxs-lookup"><span data-stu-id="43239-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="43239-112">OS</span><span class="sxs-lookup"><span data-stu-id="43239-112">PARAMETERS</span></span>

### <span data-ttu-id="43239-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43239-113">-AsJob</span></span>
<span data-ttu-id="43239-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="43239-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43239-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43239-115">-DefaultProfile</span></span>
<span data-ttu-id="43239-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43239-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43239-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="43239-117">-LoadBalancer</span></span>
<span data-ttu-id="43239-118">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="43239-118">Specifies a load balancer.</span></span>
<span data-ttu-id="43239-119">Esse cmdlet define o estado da meta do balanceador de carga que o parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="43239-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43239-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43239-120">-Confirm</span></span>
<span data-ttu-id="43239-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43239-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43239-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43239-122">-WhatIf</span></span>
<span data-ttu-id="43239-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43239-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43239-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43239-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43239-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43239-125">CommonParameters</span></span>
<span data-ttu-id="43239-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43239-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43239-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43239-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43239-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43239-128">INPUTS</span></span>

### <span data-ttu-id="43239-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="43239-130">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43239-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="43239-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43239-131">OUTPUTS</span></span>

### <span data-ttu-id="43239-132">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="43239-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43239-133">NOTES</span></span>

## <span data-ttu-id="43239-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43239-134">RELATED LINKS</span></span>

[<span data-ttu-id="43239-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="43239-136">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="43239-137">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43239-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


