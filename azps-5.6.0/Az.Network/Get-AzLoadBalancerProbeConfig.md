---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 43c3b4d17d024eaae06c7d7f891dfd2ea3e08aa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892459"
---
# <span data-ttu-id="0b776-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b776-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0b776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b776-102">SYNOPSIS</span></span>
<span data-ttu-id="0b776-103">Obtém uma configuração de sonda para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0b776-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="0b776-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b776-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b776-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b776-105">DESCRIPTION</span></span>
<span data-ttu-id="0b776-106">O cmdlet **Get-AzLoadBalancerProbeConfig** obtém uma ou mais configurações de sonda para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0b776-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="0b776-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b776-107">EXAMPLES</span></span>

### <span data-ttu-id="0b776-108">Exemplo 1: Obter a configuração de sonda de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0b776-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="0b776-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="0b776-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0b776-110">O segundo comando obtém a configuração de sonda associada chamada MyProbe do balanceador de carga no $slb.</span><span class="sxs-lookup"><span data-stu-id="0b776-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="0b776-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b776-111">PARAMETERS</span></span>

### <span data-ttu-id="0b776-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b776-112">-DefaultProfile</span></span>
<span data-ttu-id="0b776-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0b776-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b776-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b776-114">-LoadBalancer</span></span>
<span data-ttu-id="0b776-115">Especifica o balanceador de carga associado à configuração da sonda a ser obter.</span><span class="sxs-lookup"><span data-stu-id="0b776-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="0b776-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0b776-116">-Name</span></span>
<span data-ttu-id="0b776-117">Especifica o nome da configuração da sonda a ser obter.</span><span class="sxs-lookup"><span data-stu-id="0b776-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="0b776-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b776-118">CommonParameters</span></span>
<span data-ttu-id="0b776-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b776-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b776-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b776-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b776-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b776-121">INPUTS</span></span>

### <span data-ttu-id="0b776-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b776-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0b776-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b776-123">OUTPUTS</span></span>

### <span data-ttu-id="0b776-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="0b776-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="0b776-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b776-125">NOTES</span></span>

## <span data-ttu-id="0b776-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b776-126">RELATED LINKS</span></span>

[<span data-ttu-id="0b776-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b776-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b776-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b776-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0b776-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b776-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b776-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b776-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="0b776-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b776-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


