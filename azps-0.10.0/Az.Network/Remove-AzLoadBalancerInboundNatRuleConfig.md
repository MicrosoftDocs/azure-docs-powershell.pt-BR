---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775294"
---
# <span data-ttu-id="8b59e-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b59e-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8b59e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b59e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b59e-103">Remove uma configuração de regra NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8b59e-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="8b59e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b59e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b59e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b59e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b59e-106">O cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** remove uma configuração de regra NAT (conversão de endereço de rede) de entrada de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b59e-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="8b59e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b59e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b59e-108">1: excluir uma regra NAT de entrada de um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="8b59e-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="8b59e-109">O primeiro comando carrega um balanceador de carga já existente chamado "mylb" e o armazena na variável de balanceador de $load.</span><span class="sxs-lookup"><span data-stu-id="8b59e-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="8b59e-110">O segundo comando Remove a regra NAT de entrada associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8b59e-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="8b59e-111">OS</span><span class="sxs-lookup"><span data-stu-id="8b59e-111">PARAMETERS</span></span>

### <span data-ttu-id="8b59e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b59e-112">-DefaultProfile</span></span>
<span data-ttu-id="8b59e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b59e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b59e-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="8b59e-114">-LoadBalancer</span></span>
<span data-ttu-id="8b59e-115">Especifica o objeto **Loadbalancer** que contém a configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8b59e-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b59e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b59e-116">-Name</span></span>
<span data-ttu-id="8b59e-117">Especifica o nome da configuração de regra NAT de entrada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8b59e-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b59e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b59e-118">CommonParameters</span></span>
<span data-ttu-id="8b59e-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b59e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b59e-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b59e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b59e-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b59e-121">INPUTS</span></span>

### <span data-ttu-id="8b59e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b59e-122">PSLoadBalancer</span></span>
<span data-ttu-id="8b59e-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8b59e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8b59e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b59e-124">OUTPUTS</span></span>

### <span data-ttu-id="8b59e-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b59e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8b59e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b59e-126">NOTES</span></span>

## <span data-ttu-id="8b59e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b59e-127">RELATED LINKS</span></span>

[<span data-ttu-id="8b59e-128">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b59e-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8b59e-129">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b59e-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8b59e-130">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b59e-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8b59e-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b59e-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


