---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee831cf3f2b6441bde55dc458d6b9af33f4b42e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426895"
---
# <span data-ttu-id="21b46-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b46-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="21b46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21b46-102">SYNOPSIS</span></span>
<span data-ttu-id="21b46-103">Remove uma configuração de regra NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="21b46-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21b46-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21b46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21b46-105">DESCRIPTION</span></span>
<span data-ttu-id="21b46-106">O cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** remove uma configuração de regra NAT (conversão de endereço de rede) de entrada de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="21b46-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="21b46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21b46-107">EXAMPLES</span></span>

### <span data-ttu-id="21b46-108">1: excluir uma regra NAT de entrada de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="21b46-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="21b46-109">O primeiro comando carrega um balanceador de carga já existente chamado "mylb" e o armazena na variável de balanceador de $load.</span><span class="sxs-lookup"><span data-stu-id="21b46-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="21b46-110">O segundo comando Remove a regra NAT de entrada associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="21b46-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="21b46-111">OS</span><span class="sxs-lookup"><span data-stu-id="21b46-111">PARAMETERS</span></span>

### <span data-ttu-id="21b46-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="21b46-112">-LoadBalancer</span></span>
<span data-ttu-id="21b46-113">Especifica o objeto **Loadbalancer** que contém a configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="21b46-113">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21b46-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="21b46-114">-Name</span></span>
<span data-ttu-id="21b46-115">Especifica o nome da configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="21b46-115">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21b46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b46-116">-DefaultProfile</span></span>
<span data-ttu-id="21b46-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21b46-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21b46-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b46-118">CommonParameters</span></span>
<span data-ttu-id="21b46-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b46-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b46-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b46-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b46-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21b46-121">INPUTS</span></span>

### <span data-ttu-id="21b46-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21b46-122">PSLoadBalancer</span></span>
<span data-ttu-id="21b46-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="21b46-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="21b46-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21b46-124">OUTPUTS</span></span>

### <span data-ttu-id="21b46-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21b46-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21b46-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21b46-126">NOTES</span></span>

## <span data-ttu-id="21b46-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21b46-127">RELATED LINKS</span></span>

[<span data-ttu-id="21b46-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b46-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="21b46-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b46-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="21b46-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b46-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="21b46-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b46-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


