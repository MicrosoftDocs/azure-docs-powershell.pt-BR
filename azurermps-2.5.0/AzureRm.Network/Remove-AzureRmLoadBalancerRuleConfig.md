---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786276"
---
# <span data-ttu-id="fbacf-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbacf-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="fbacf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbacf-102">SYNOPSIS</span></span>
<span data-ttu-id="fbacf-103">Remove uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fbacf-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbacf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbacf-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbacf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbacf-105">DESCRIPTION</span></span>
<span data-ttu-id="fbacf-106">O cmdlet **Remove-AzureRmLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbacf-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="fbacf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbacf-107">EXAMPLES</span></span>

### <span data-ttu-id="fbacf-108">Exemplo 1: remover uma configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="fbacf-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="fbacf-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="fbacf-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="fbacf-110">O segundo comando Remove a configuração de regra nomeada MyLBruleName do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="fbacf-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="fbacf-111">OS</span><span class="sxs-lookup"><span data-stu-id="fbacf-111">PARAMETERS</span></span>

### <span data-ttu-id="fbacf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbacf-112">-DefaultProfile</span></span>
<span data-ttu-id="fbacf-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbacf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbacf-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="fbacf-114">-LoadBalancer</span></span>
<span data-ttu-id="fbacf-115">Especifica o objeto **Loadbalancer** que contém a configuração de regra que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fbacf-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fbacf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbacf-116">-Name</span></span>
<span data-ttu-id="fbacf-117">Especifica o nome da configuração de regra de balanceamento de carga que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fbacf-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbacf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbacf-118">CommonParameters</span></span>
<span data-ttu-id="fbacf-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbacf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbacf-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbacf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbacf-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbacf-121">INPUTS</span></span>

### <span data-ttu-id="fbacf-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbacf-122">PSLoadBalancer</span></span>
<span data-ttu-id="fbacf-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fbacf-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fbacf-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbacf-124">OUTPUTS</span></span>

### <span data-ttu-id="fbacf-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbacf-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fbacf-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbacf-126">NOTES</span></span>

## <span data-ttu-id="fbacf-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbacf-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbacf-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbacf-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fbacf-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbacf-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fbacf-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbacf-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fbacf-131">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbacf-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fbacf-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbacf-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


