---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: da7004c8737bf454ea8847b529f003f5b1909f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771750"
---
# <span data-ttu-id="53cf9-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="53cf9-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="53cf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="53cf9-103">Obtém uma ou mais configurações de pool de NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53cf9-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="53cf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53cf9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53cf9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="53cf9-106">O cmdlet **Get-AzLoadBalancerInboundNatPoolConfig** Obtém uma ou mais configurações de pool de NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53cf9-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="53cf9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="53cf9-108">1: obter</span><span class="sxs-lookup"><span data-stu-id="53cf9-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="53cf9-109">OS</span><span class="sxs-lookup"><span data-stu-id="53cf9-109">PARAMETERS</span></span>

### <span data-ttu-id="53cf9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53cf9-110">-DefaultProfile</span></span>
<span data-ttu-id="53cf9-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53cf9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53cf9-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="53cf9-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="53cf9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="53cf9-113">-Name</span></span>
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

### <span data-ttu-id="53cf9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cf9-114">CommonParameters</span></span>
<span data-ttu-id="53cf9-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53cf9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cf9-116">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53cf9-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cf9-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53cf9-117">INPUTS</span></span>

### <span data-ttu-id="53cf9-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53cf9-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="53cf9-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53cf9-119">OUTPUTS</span></span>

### <span data-ttu-id="53cf9-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="53cf9-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="53cf9-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53cf9-121">NOTES</span></span>

## <span data-ttu-id="53cf9-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53cf9-122">RELATED LINKS</span></span>

[<span data-ttu-id="53cf9-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="53cf9-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="53cf9-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="53cf9-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="53cf9-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="53cf9-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="53cf9-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="53cf9-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
