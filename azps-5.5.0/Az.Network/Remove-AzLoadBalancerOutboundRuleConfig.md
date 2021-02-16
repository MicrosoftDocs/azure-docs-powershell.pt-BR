---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113455"
---
# <span data-ttu-id="55a00-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55a00-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="55a00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55a00-102">SYNOPSIS</span></span>
<span data-ttu-id="55a00-103">Remove uma configuração de regra de saída de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55a00-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="55a00-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55a00-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a00-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="55a00-105">DESCRIPTION</span></span>
<span data-ttu-id="55a00-106">O cmdlet **Remove-AzLoadBalancerOutboundRuleConfig** remove uma configuração de regra de saída de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="55a00-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="55a00-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55a00-107">EXAMPLES</span></span>

### <span data-ttu-id="55a00-108">Exemplo 1: Excluir uma regra de saída de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="55a00-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="55a00-109">O primeiro comando obtém o balanceador de carga associado à configuração de regra de saída que você deseja remover e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="55a00-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="55a00-110">O segundo comando remove a configuração da regra de saída associada do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55a00-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="55a00-111">O terceiro comando atualiza o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55a00-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="55a00-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55a00-112">PARAMETERS</span></span>

### <span data-ttu-id="55a00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a00-113">-DefaultProfile</span></span>
<span data-ttu-id="55a00-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55a00-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a00-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55a00-115">-LoadBalancer</span></span>
<span data-ttu-id="55a00-116">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55a00-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="55a00-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="55a00-117">-Name</span></span>
<span data-ttu-id="55a00-118">O Nome da regra de saída</span><span class="sxs-lookup"><span data-stu-id="55a00-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="55a00-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55a00-119">-Confirm</span></span>
<span data-ttu-id="55a00-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55a00-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a00-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a00-121">-WhatIf</span></span>
<span data-ttu-id="55a00-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55a00-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a00-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55a00-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a00-124">CommonParameters</span></span>
<span data-ttu-id="55a00-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a00-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a00-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a00-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="55a00-127">INPUTS</span></span>

### <span data-ttu-id="55a00-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55a00-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55a00-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="55a00-129">OUTPUTS</span></span>

### <span data-ttu-id="55a00-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55a00-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55a00-131">Notas</span><span class="sxs-lookup"><span data-stu-id="55a00-131">NOTES</span></span>

## <span data-ttu-id="55a00-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55a00-132">RELATED LINKS</span></span>

[<span data-ttu-id="55a00-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55a00-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="55a00-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55a00-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="55a00-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55a00-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="55a00-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55a00-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
