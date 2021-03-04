---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 053f86f0b29346c98f60a3160a8e1f2a51ab0e14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891131"
---
# <span data-ttu-id="d1677-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1677-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d1677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1677-102">SYNOPSIS</span></span>
<span data-ttu-id="d1677-103">Remove uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d1677-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d1677-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d1677-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1677-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d1677-105">DESCRIPTION</span></span>
<span data-ttu-id="d1677-106">O cmdlet **Remove-AzLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1677-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d1677-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1677-107">EXAMPLES</span></span>

### <span data-ttu-id="d1677-108">Exemplo 1: Remover uma configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d1677-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d1677-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $loadbalancer de carga.</span><span class="sxs-lookup"><span data-stu-id="d1677-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="d1677-110">O segundo comando remove a configuração de regra chamada MyLBruleName do balanceador de carga no $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="d1677-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d1677-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d1677-111">PARAMETERS</span></span>

### <span data-ttu-id="d1677-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1677-112">-DefaultProfile</span></span>
<span data-ttu-id="d1677-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d1677-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1677-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1677-114">-LoadBalancer</span></span>
<span data-ttu-id="d1677-115">Especifica o **objeto LoadBalancer** que contém a configuração de regra que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d1677-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d1677-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d1677-116">-Name</span></span>
<span data-ttu-id="d1677-117">Especifica o nome da configuração de regra do balanceador de carga que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d1677-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d1677-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1677-118">-Confirm</span></span>
<span data-ttu-id="d1677-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1677-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1677-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1677-120">-WhatIf</span></span>
<span data-ttu-id="d1677-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1677-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1677-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1677-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1677-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1677-123">CommonParameters</span></span>
<span data-ttu-id="d1677-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1677-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1677-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1677-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1677-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1677-126">INPUTS</span></span>

### <span data-ttu-id="d1677-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1677-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d1677-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d1677-128">OUTPUTS</span></span>

### <span data-ttu-id="d1677-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1677-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d1677-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="d1677-130">NOTES</span></span>

## <span data-ttu-id="d1677-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1677-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1677-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1677-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d1677-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d1677-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d1677-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1677-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d1677-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1677-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d1677-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1677-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


