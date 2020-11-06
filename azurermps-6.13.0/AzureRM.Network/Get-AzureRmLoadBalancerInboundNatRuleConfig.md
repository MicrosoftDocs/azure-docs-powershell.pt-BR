---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 378d9521e309629bdb9e6ee58cfc1cd06fd9ef7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428067"
---
# <span data-ttu-id="00c00-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c00-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="00c00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00c00-102">SYNOPSIS</span></span>
<span data-ttu-id="00c00-103">Obtém uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="00c00-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00c00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00c00-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c00-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00c00-105">DESCRIPTION</span></span>
<span data-ttu-id="00c00-106">O cmdlet **Get-AzureRmLoadBalancerInboundNatRuleConfig** Obtém uma ou mais regras de entrada de NAT (conversão de endereço de rede) em um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="00c00-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="00c00-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00c00-107">EXAMPLES</span></span>

### <span data-ttu-id="00c00-108">Exemplo 1: obter uma configuração de regra NAT de entrada</span><span class="sxs-lookup"><span data-stu-id="00c00-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="00c00-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="00c00-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="00c00-110">O segundo comando obtém a regra NAT associada chamada MyInboundNatRule1 do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="00c00-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="00c00-111">OS</span><span class="sxs-lookup"><span data-stu-id="00c00-111">PARAMETERS</span></span>

### <span data-ttu-id="00c00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c00-112">-DefaultProfile</span></span>
<span data-ttu-id="00c00-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00c00-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c00-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="00c00-114">-LoadBalancer</span></span>
<span data-ttu-id="00c00-115">Especifica o balanceador de carga que está associado à configuração de regra NAT de entrada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="00c00-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="00c00-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c00-116">-Name</span></span>
<span data-ttu-id="00c00-117">Especifica o nome da configuração de regra NAT de entrada a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="00c00-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="00c00-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c00-118">CommonParameters</span></span>
<span data-ttu-id="00c00-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c00-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c00-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c00-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c00-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00c00-121">INPUTS</span></span>

### <span data-ttu-id="00c00-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00c00-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="00c00-123">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00c00-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="00c00-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00c00-124">OUTPUTS</span></span>

### <span data-ttu-id="00c00-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="00c00-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="00c00-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00c00-126">NOTES</span></span>

## <span data-ttu-id="00c00-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00c00-127">RELATED LINKS</span></span>

[<span data-ttu-id="00c00-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00c00-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="00c00-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c00-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="00c00-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c00-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="00c00-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00c00-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


