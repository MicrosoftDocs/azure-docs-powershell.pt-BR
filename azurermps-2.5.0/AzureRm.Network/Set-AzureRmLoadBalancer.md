---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 7719847f578b540fd2c8bba93a378c4377fecab8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786272"
---
# <span data-ttu-id="a30f7-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="a30f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a30f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a30f7-103">Define o estado da meta para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a30f7-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a30f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a30f7-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a30f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a30f7-105">DESCRIPTION</span></span>
<span data-ttu-id="a30f7-106">O cmdlet **set-AzureRmLoadBalancer** define o estado da meta para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="a30f7-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="a30f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a30f7-107">EXAMPLES</span></span>

### <span data-ttu-id="a30f7-108">Exemplo 1: modificar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a30f7-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a30f7-109">O primeiro comando obtém o balanceador de carga chamado NRPLB e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="a30f7-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="a30f7-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para Add-AzureRmLoadBalancerInboundNatRuleConfig, que adiciona uma regra NAT de entrada chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="a30f7-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="a30f7-111">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancer** , que atualiza a configuração do balanceador de carga e salva-o.</span><span class="sxs-lookup"><span data-stu-id="a30f7-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="a30f7-112">OS</span><span class="sxs-lookup"><span data-stu-id="a30f7-112">PARAMETERS</span></span>

### <span data-ttu-id="a30f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a30f7-113">-AsJob</span></span>
<span data-ttu-id="a30f7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a30f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a30f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30f7-115">-DefaultProfile</span></span>
<span data-ttu-id="a30f7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a30f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a30f7-117">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-117">-LoadBalancer</span></span>
<span data-ttu-id="a30f7-118">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a30f7-118">Specifies a load balancer.</span></span>
<span data-ttu-id="a30f7-119">Esse cmdlet define o estado da meta do balanceador de carga que o parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a30f7-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a30f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30f7-120">CommonParameters</span></span>
<span data-ttu-id="a30f7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a30f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30f7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a30f7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30f7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a30f7-123">INPUTS</span></span>

### <span data-ttu-id="a30f7-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-124">PSLoadBalancer</span></span>
<span data-ttu-id="a30f7-125">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a30f7-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a30f7-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a30f7-126">OUTPUTS</span></span>

### <span data-ttu-id="a30f7-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a30f7-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a30f7-128">NOTES</span></span>

## <span data-ttu-id="a30f7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a30f7-129">RELATED LINKS</span></span>

[<span data-ttu-id="a30f7-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a30f7-131">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="a30f7-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a30f7-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


