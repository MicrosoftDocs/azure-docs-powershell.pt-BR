---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114088"
---
# <span data-ttu-id="3eb72-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="3eb72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3eb72-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb72-103">Atualiza um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3eb72-103">Updates a load balancer.</span></span>

## <span data-ttu-id="3eb72-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eb72-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb72-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3eb72-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb72-106">O **cmdlet Set-AzLoadBalancer** atualiza um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3eb72-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="3eb72-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3eb72-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb72-108">Exemplo 1: Modificar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="3eb72-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="3eb72-109">O primeiro comando obtém o balanceador de carga chamado NRPLB e o armazena na variável $slb dados.</span><span class="sxs-lookup"><span data-stu-id="3eb72-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="3eb72-110">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerInboundNatRuleConfig, que adiciona uma regra NAT de entrada chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="3eb72-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="3eb72-111">O terceiro comando passa o balanceador de carga para **o Set-AzLoadBalancer,** que atualiza a configuração do balanceador de carga e salva-a.</span><span class="sxs-lookup"><span data-stu-id="3eb72-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="3eb72-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eb72-112">PARAMETERS</span></span>

### <span data-ttu-id="3eb72-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eb72-113">-AsJob</span></span>
<span data-ttu-id="3eb72-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3eb72-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eb72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb72-115">-DefaultProfile</span></span>
<span data-ttu-id="3eb72-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3eb72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb72-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-117">-LoadBalancer</span></span>
<span data-ttu-id="3eb72-118">Especifica um objeto de balanceador de carga que representa o estado ao qual o balanceador de carga deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="3eb72-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="3eb72-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3eb72-119">-Confirm</span></span>
<span data-ttu-id="3eb72-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eb72-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb72-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb72-121">-WhatIf</span></span>
<span data-ttu-id="3eb72-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3eb72-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eb72-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3eb72-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb72-124">CommonParameters</span></span>
<span data-ttu-id="3eb72-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb72-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb72-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb72-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="3eb72-127">INPUTS</span></span>

### <span data-ttu-id="3eb72-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3eb72-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="3eb72-129">OUTPUTS</span></span>

### <span data-ttu-id="3eb72-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3eb72-131">Notas</span><span class="sxs-lookup"><span data-stu-id="3eb72-131">NOTES</span></span>

## <span data-ttu-id="3eb72-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3eb72-132">RELATED LINKS</span></span>

[<span data-ttu-id="3eb72-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3eb72-134">Novo-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="3eb72-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3eb72-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


