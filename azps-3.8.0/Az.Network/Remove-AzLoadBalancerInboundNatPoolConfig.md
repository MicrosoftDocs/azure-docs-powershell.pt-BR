---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944035"
---
# <span data-ttu-id="c8ef1-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c8ef1-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c8ef1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ef1-103">Remove uma configuração de pool NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="c8ef1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8ef1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8ef1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ef1-106">O cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** remove uma configuração de pool NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="c8ef1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ef1-108">1: remover</span><span class="sxs-lookup"><span data-stu-id="c8ef1-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="c8ef1-109">OS</span><span class="sxs-lookup"><span data-stu-id="c8ef1-109">PARAMETERS</span></span>

### <span data-ttu-id="c8ef1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ef1-110">-DefaultProfile</span></span>
<span data-ttu-id="c8ef1-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8ef1-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="c8ef1-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="c8ef1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8ef1-113">-Name</span></span>
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

### <span data-ttu-id="c8ef1-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8ef1-114">-Confirm</span></span>
<span data-ttu-id="c8ef1-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ef1-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8ef1-116">-WhatIf</span></span>
<span data-ttu-id="c8ef1-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8ef1-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ef1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ef1-119">CommonParameters</span></span>
<span data-ttu-id="c8ef1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ef1-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8ef1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ef1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8ef1-122">INPUTS</span></span>

### <span data-ttu-id="c8ef1-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8ef1-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c8ef1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8ef1-124">OUTPUTS</span></span>

### <span data-ttu-id="c8ef1-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8ef1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c8ef1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8ef1-126">NOTES</span></span>

## <span data-ttu-id="c8ef1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8ef1-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8ef1-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c8ef1-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c8ef1-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c8ef1-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c8ef1-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c8ef1-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c8ef1-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c8ef1-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
