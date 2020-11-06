---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 38f6223fdf1dc230dbd34310b7eda2ab45e2d4b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602053"
---
# <span data-ttu-id="e233d-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e233d-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e233d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e233d-102">SYNOPSIS</span></span>
<span data-ttu-id="e233d-103">Remove uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e233d-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e233d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e233d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e233d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e233d-105">DESCRIPTION</span></span>
<span data-ttu-id="e233d-106">O cmdlet **Remove-AzureRmLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="e233d-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e233d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e233d-107">EXAMPLES</span></span>

### <span data-ttu-id="e233d-108">Exemplo 1: remover uma configuração de regra de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="e233d-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e233d-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e233d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="e233d-110">O segundo comando Remove a configuração de regra nomeada MyLBruleName do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e233d-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e233d-111">OS</span><span class="sxs-lookup"><span data-stu-id="e233d-111">PARAMETERS</span></span>

### <span data-ttu-id="e233d-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="e233d-112">-LoadBalancer</span></span>
<span data-ttu-id="e233d-113">Especifica o objeto **Loadbalancer** que contém a configuração de regra que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e233d-113">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e233d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e233d-114">-Name</span></span>
<span data-ttu-id="e233d-115">Especifica o nome da configuração de regra de balanceamento de carga que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e233d-115">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e233d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e233d-116">-DefaultProfile</span></span>
<span data-ttu-id="e233d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e233d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e233d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e233d-118">CommonParameters</span></span>
<span data-ttu-id="e233d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e233d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e233d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e233d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e233d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e233d-121">INPUTS</span></span>

### <span data-ttu-id="e233d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e233d-122">PSLoadBalancer</span></span>
<span data-ttu-id="e233d-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e233d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e233d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e233d-124">OUTPUTS</span></span>

### <span data-ttu-id="e233d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e233d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e233d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e233d-126">NOTES</span></span>

## <span data-ttu-id="e233d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e233d-127">RELATED LINKS</span></span>

[<span data-ttu-id="e233d-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e233d-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e233d-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e233d-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e233d-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e233d-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e233d-131">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e233d-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="e233d-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e233d-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


