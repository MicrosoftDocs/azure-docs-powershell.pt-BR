---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b09aeb7288f69d0edc678578bbcc91306f5b0c2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441466"
---
# <span data-ttu-id="ae78d-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae78d-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ae78d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae78d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae78d-103">Obtém a configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ae78d-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae78d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae78d-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae78d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae78d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae78d-106">O cmdlet **Get-AzureRmLoadBalancerRuleConfig** Obtém uma ou mais configurações de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ae78d-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="ae78d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae78d-107">EXAMPLES</span></span>

### <span data-ttu-id="ae78d-108">Exemplo 1: obter a configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ae78d-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="ae78d-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="ae78d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="ae78d-110">O segundo comando obtém a configuração de regra associada nomeada MyLBrulename do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="ae78d-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="ae78d-111">OS</span><span class="sxs-lookup"><span data-stu-id="ae78d-111">PARAMETERS</span></span>

### <span data-ttu-id="ae78d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae78d-112">-DefaultProfile</span></span>
<span data-ttu-id="ae78d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae78d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae78d-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="ae78d-114">-LoadBalancer</span></span>
<span data-ttu-id="ae78d-115">Especifica o balanceador de carga associado à configuração de regra a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="ae78d-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="ae78d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae78d-116">-Name</span></span>
<span data-ttu-id="ae78d-117">Especifica o nome da configuração da regra a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="ae78d-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="ae78d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae78d-118">CommonParameters</span></span>
<span data-ttu-id="ae78d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae78d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae78d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae78d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae78d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae78d-121">INPUTS</span></span>

### <span data-ttu-id="ae78d-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae78d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ae78d-123">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae78d-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="ae78d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae78d-124">OUTPUTS</span></span>

### <span data-ttu-id="ae78d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="ae78d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="ae78d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae78d-126">NOTES</span></span>

## <span data-ttu-id="ae78d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae78d-127">RELATED LINKS</span></span>

[<span data-ttu-id="ae78d-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae78d-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ae78d-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae78d-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ae78d-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae78d-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ae78d-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae78d-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)

