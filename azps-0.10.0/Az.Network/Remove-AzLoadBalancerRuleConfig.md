---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775287"
---
# <span data-ttu-id="a5e9d-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5e9d-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a5e9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e9d-103">Remove uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a5e9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5e9d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e9d-106">O cmdlet **Remove-AzLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a5e9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5e9d-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e9d-108">Exemplo 1: remover uma configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="a5e9d-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a5e9d-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="a5e9d-110">O segundo comando Remove a configuração de regra nomeada MyLBruleName do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a5e9d-111">OS</span><span class="sxs-lookup"><span data-stu-id="a5e9d-111">PARAMETERS</span></span>

### <span data-ttu-id="a5e9d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e9d-112">-DefaultProfile</span></span>
<span data-ttu-id="a5e9d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e9d-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="a5e9d-114">-LoadBalancer</span></span>
<span data-ttu-id="a5e9d-115">Especifica o objeto **Loadbalancer** que contém a configuração de regra que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5e9d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5e9d-116">-Name</span></span>
<span data-ttu-id="a5e9d-117">Especifica o nome da configuração de regra de balanceamento de carga que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5e9d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e9d-118">CommonParameters</span></span>
<span data-ttu-id="a5e9d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e9d-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e9d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e9d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5e9d-121">INPUTS</span></span>

### <span data-ttu-id="a5e9d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5e9d-122">PSLoadBalancer</span></span>
<span data-ttu-id="a5e9d-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a5e9d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a5e9d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5e9d-124">OUTPUTS</span></span>

### <span data-ttu-id="a5e9d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5e9d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a5e9d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5e9d-126">NOTES</span></span>

## <span data-ttu-id="a5e9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5e9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a5e9d-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5e9d-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a5e9d-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5e9d-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a5e9d-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5e9d-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a5e9d-131">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5e9d-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a5e9d-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5e9d-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


