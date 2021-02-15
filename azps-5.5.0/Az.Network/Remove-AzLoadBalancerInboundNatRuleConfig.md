---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114114"
---
# <span data-ttu-id="74b01-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74b01-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="74b01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74b01-102">SYNOPSIS</span></span>
<span data-ttu-id="74b01-103">Remove uma configuração de regra NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="74b01-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="74b01-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74b01-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b01-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="74b01-105">DESCRIPTION</span></span>
<span data-ttu-id="74b01-106">O cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** remove uma configuração de regra nat (conversão de endereço de rede de entrada) de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="74b01-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="74b01-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74b01-107">EXAMPLES</span></span>

### <span data-ttu-id="74b01-108">1: Excluir uma regra NAT de entrada de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="74b01-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="74b01-109">O primeiro comando carrega um balanceador de carga já existente chamado "mylb" e o armazena na variável $load balanceador.</span><span class="sxs-lookup"><span data-stu-id="74b01-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="74b01-110">O segundo comando remove a regra NAT de entrada associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="74b01-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="74b01-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74b01-111">PARAMETERS</span></span>

### <span data-ttu-id="74b01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b01-112">-DefaultProfile</span></span>
<span data-ttu-id="74b01-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="74b01-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b01-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74b01-114">-LoadBalancer</span></span>
<span data-ttu-id="74b01-115">Especifica o **objeto LoadBalancer** que contém a configuração de regra NAT de entrada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="74b01-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="74b01-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="74b01-116">-Name</span></span>
<span data-ttu-id="74b01-117">Especifica o nome da configuração da regra NAT de entrada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="74b01-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="74b01-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74b01-118">-Confirm</span></span>
<span data-ttu-id="74b01-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b01-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b01-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b01-120">-WhatIf</span></span>
<span data-ttu-id="74b01-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74b01-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74b01-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74b01-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b01-123">CommonParameters</span></span>
<span data-ttu-id="74b01-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b01-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b01-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b01-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="74b01-126">INPUTS</span></span>

### <span data-ttu-id="74b01-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74b01-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="74b01-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="74b01-128">OUTPUTS</span></span>

### <span data-ttu-id="74b01-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74b01-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="74b01-130">Notas</span><span class="sxs-lookup"><span data-stu-id="74b01-130">NOTES</span></span>

## <span data-ttu-id="74b01-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74b01-131">RELATED LINKS</span></span>

[<span data-ttu-id="74b01-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74b01-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74b01-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74b01-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74b01-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74b01-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74b01-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74b01-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


