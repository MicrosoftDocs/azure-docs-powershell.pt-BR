---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943335"
---
# <span data-ttu-id="6d519-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d519-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="6d519-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d519-102">SYNOPSIS</span></span>
<span data-ttu-id="6d519-103">Obtém uma configuração de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6d519-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="6d519-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d519-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d519-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d519-105">DESCRIPTION</span></span>
<span data-ttu-id="6d519-106">O cmdlet **Get-AzLoadBalancerProbeConfig** Obtém uma ou mais configurações de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6d519-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="6d519-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d519-107">EXAMPLES</span></span>

### <span data-ttu-id="6d519-108">Exemplo 1: obter a configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="6d519-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="6d519-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="6d519-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6d519-110">O segundo comando obtém a configuração de teste associada chamada myprobe do balanceador de carga em $slb.</span><span class="sxs-lookup"><span data-stu-id="6d519-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="6d519-111">OS</span><span class="sxs-lookup"><span data-stu-id="6d519-111">PARAMETERS</span></span>

### <span data-ttu-id="6d519-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d519-112">-DefaultProfile</span></span>
<span data-ttu-id="6d519-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d519-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d519-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="6d519-114">-LoadBalancer</span></span>
<span data-ttu-id="6d519-115">Especifica o balanceador de carga associado à configuração de sonda a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6d519-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="6d519-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d519-116">-Name</span></span>
<span data-ttu-id="6d519-117">Especifica o nome da configuração de teste a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6d519-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="6d519-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d519-118">CommonParameters</span></span>
<span data-ttu-id="6d519-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d519-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d519-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d519-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d519-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d519-121">INPUTS</span></span>

### <span data-ttu-id="6d519-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d519-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d519-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d519-123">OUTPUTS</span></span>

### <span data-ttu-id="6d519-124">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="6d519-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="6d519-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d519-125">NOTES</span></span>

## <span data-ttu-id="6d519-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d519-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d519-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d519-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d519-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d519-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6d519-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d519-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d519-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d519-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d519-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d519-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


