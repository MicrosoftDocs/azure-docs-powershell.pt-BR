---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262467"
---
# <span data-ttu-id="dfd1c-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="dfd1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd1c-103">Obtém uma ou mais configurações de pool de NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="dfd1c-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="dfd1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfd1c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd1c-106">O cmdlet **Get-AzLoadBalancerInboundNatPoolConfig** Obtém uma ou mais configurações de pool de NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="dfd1c-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="dfd1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfd1c-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd1c-108">1: obter</span><span class="sxs-lookup"><span data-stu-id="dfd1c-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="dfd1c-109">OS</span><span class="sxs-lookup"><span data-stu-id="dfd1c-109">PARAMETERS</span></span>

### <span data-ttu-id="dfd1c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd1c-110">-DefaultProfile</span></span>
<span data-ttu-id="dfd1c-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd1c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd1c-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="dfd1c-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="dfd1c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfd1c-113">-Name</span></span>
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

### <span data-ttu-id="dfd1c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd1c-114">CommonParameters</span></span>
<span data-ttu-id="dfd1c-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd1c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd1c-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfd1c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd1c-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfd1c-117">INPUTS</span></span>

### <span data-ttu-id="dfd1c-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dfd1c-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dfd1c-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfd1c-119">OUTPUTS</span></span>

### <span data-ttu-id="dfd1c-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="dfd1c-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="dfd1c-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfd1c-121">NOTES</span></span>

## <span data-ttu-id="dfd1c-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfd1c-122">RELATED LINKS</span></span>

[<span data-ttu-id="dfd1c-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfd1c-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfd1c-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfd1c-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfd1c-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
