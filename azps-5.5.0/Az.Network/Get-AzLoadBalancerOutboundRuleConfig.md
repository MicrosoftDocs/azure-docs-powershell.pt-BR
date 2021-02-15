---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115181"
---
# <span data-ttu-id="0c666-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c666-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="0c666-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c666-102">SYNOPSIS</span></span>
<span data-ttu-id="0c666-103">Obtém uma configuração de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0c666-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="0c666-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c666-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c666-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c666-105">DESCRIPTION</span></span>
<span data-ttu-id="0c666-106">O cmdlet **Get-AzLoadBalancerOutboundRuleConfig** obtém uma configuração de regra de saída ou uma lista de configurações de regra de saída em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0c666-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="0c666-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c666-107">EXAMPLES</span></span>

### <span data-ttu-id="0c666-108">Exemplo 1: Obter uma configuração de regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0c666-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="0c666-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="0c666-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0c666-110">O segundo comando obtém a configuração de regra de saída chamada MyRule associada a esse balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0c666-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="0c666-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c666-111">PARAMETERS</span></span>

### <span data-ttu-id="0c666-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c666-112">-DefaultProfile</span></span>
<span data-ttu-id="0c666-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c666-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c666-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c666-114">-LoadBalancer</span></span>
<span data-ttu-id="0c666-115">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0c666-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="0c666-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c666-116">-Name</span></span>
<span data-ttu-id="0c666-117">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="0c666-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="0c666-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c666-118">CommonParameters</span></span>
<span data-ttu-id="0c666-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c666-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c666-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c666-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c666-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c666-121">INPUTS</span></span>

### <span data-ttu-id="0c666-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c666-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0c666-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c666-123">OUTPUTS</span></span>

### <span data-ttu-id="0c666-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="0c666-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="0c666-125">Notas</span><span class="sxs-lookup"><span data-stu-id="0c666-125">NOTES</span></span>

## <span data-ttu-id="0c666-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c666-126">RELATED LINKS</span></span>

[<span data-ttu-id="0c666-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c666-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0c666-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c666-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0c666-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c666-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0c666-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c666-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
