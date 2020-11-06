---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428049"
---
# <span data-ttu-id="f7ed6-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7ed6-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f7ed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ed6-103">Remove uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7ed6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7ed6-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7ed6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ed6-106">O cmdlet **Remove-AzureRmLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f7ed6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ed6-108">Exemplo 1: remover uma configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f7ed6-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f7ed6-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="f7ed6-110">O segundo comando Remove a configuração de regra nomeada MyLBruleName do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f7ed6-111">OS</span><span class="sxs-lookup"><span data-stu-id="f7ed6-111">PARAMETERS</span></span>

### <span data-ttu-id="f7ed6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ed6-112">-DefaultProfile</span></span>
<span data-ttu-id="f7ed6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ed6-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f7ed6-114">-LoadBalancer</span></span>
<span data-ttu-id="f7ed6-115">Especifica o objeto **Loadbalancer** que contém a configuração de regra que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f7ed6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7ed6-116">-Name</span></span>
<span data-ttu-id="f7ed6-117">Especifica o nome da configuração de regra de balanceamento de carga que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f7ed6-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f7ed6-118">-Confirm</span></span>
<span data-ttu-id="f7ed6-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ed6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ed6-120">-WhatIf</span></span>
<span data-ttu-id="f7ed6-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7ed6-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ed6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ed6-123">CommonParameters</span></span>
<span data-ttu-id="f7ed6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ed6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ed6-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ed6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ed6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7ed6-126">INPUTS</span></span>

### <span data-ttu-id="f7ed6-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ed6-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="f7ed6-128">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7ed6-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="f7ed6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7ed6-129">OUTPUTS</span></span>

### <span data-ttu-id="f7ed6-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ed6-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f7ed6-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7ed6-131">NOTES</span></span>

## <span data-ttu-id="f7ed6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7ed6-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7ed6-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7ed6-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f7ed6-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7ed6-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f7ed6-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7ed6-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f7ed6-136">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7ed6-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f7ed6-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7ed6-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


