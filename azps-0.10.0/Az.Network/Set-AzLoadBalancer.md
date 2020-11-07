---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776544"
---
# <span data-ttu-id="21dc2-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="21dc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="21dc2-103">Define o estado da meta para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="21dc2-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="21dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21dc2-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21dc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="21dc2-106">O cmdlet **set-AzLoadBalancer** define o estado da meta para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="21dc2-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="21dc2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="21dc2-108">Exemplo 1: modificar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="21dc2-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="21dc2-109">O primeiro comando obtém o balanceador de carga chamado NRPLB e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="21dc2-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="21dc2-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzLoadBalancerInboundNatRuleConfig, que adiciona uma regra NAT de entrada chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="21dc2-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="21dc2-111">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancer** , que atualiza a configuração do balanceador de carga e salva-o.</span><span class="sxs-lookup"><span data-stu-id="21dc2-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="21dc2-112">OS</span><span class="sxs-lookup"><span data-stu-id="21dc2-112">PARAMETERS</span></span>

### <span data-ttu-id="21dc2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21dc2-113">-AsJob</span></span>
<span data-ttu-id="21dc2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21dc2-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="21dc2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21dc2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc2-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-117">-LoadBalancer</span></span>
<span data-ttu-id="21dc2-118">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="21dc2-118">Specifies a load balancer.</span></span>
<span data-ttu-id="21dc2-119">Esse cmdlet define o estado da meta do balanceador de carga que o parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21dc2-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21dc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21dc2-120">CommonParameters</span></span>
<span data-ttu-id="21dc2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21dc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21dc2-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21dc2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21dc2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21dc2-123">INPUTS</span></span>

### <span data-ttu-id="21dc2-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-124">PSLoadBalancer</span></span>
<span data-ttu-id="21dc2-125">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="21dc2-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="21dc2-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21dc2-126">OUTPUTS</span></span>

### <span data-ttu-id="21dc2-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21dc2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21dc2-128">NOTES</span></span>

## <span data-ttu-id="21dc2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21dc2-129">RELATED LINKS</span></span>

[<span data-ttu-id="21dc2-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="21dc2-131">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="21dc2-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21dc2-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


