---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259832"
---
# <span data-ttu-id="2d36f-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2d36f-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="2d36f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d36f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d36f-103">Remove uma configuração de pool NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2d36f-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="2d36f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d36f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d36f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d36f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d36f-106">O cmdlet **Remove-AzLoadBalancerInboundNatPoolConfig** remove uma configuração de pool NAT de entrada de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2d36f-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="2d36f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d36f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d36f-108">1: remover</span><span class="sxs-lookup"><span data-stu-id="2d36f-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="2d36f-109">OS</span><span class="sxs-lookup"><span data-stu-id="2d36f-109">PARAMETERS</span></span>

### <span data-ttu-id="2d36f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d36f-110">-DefaultProfile</span></span>
<span data-ttu-id="2d36f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d36f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d36f-112">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="2d36f-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="2d36f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d36f-113">-Name</span></span>
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

### <span data-ttu-id="2d36f-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d36f-114">-Confirm</span></span>
<span data-ttu-id="2d36f-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d36f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d36f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d36f-116">-WhatIf</span></span>
<span data-ttu-id="2d36f-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d36f-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d36f-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d36f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d36f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d36f-119">CommonParameters</span></span>
<span data-ttu-id="2d36f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d36f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d36f-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d36f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d36f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d36f-122">INPUTS</span></span>

### <span data-ttu-id="2d36f-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d36f-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2d36f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d36f-124">OUTPUTS</span></span>

### <span data-ttu-id="2d36f-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d36f-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2d36f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d36f-126">NOTES</span></span>

## <span data-ttu-id="2d36f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d36f-127">RELATED LINKS</span></span>

[<span data-ttu-id="2d36f-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2d36f-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="2d36f-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2d36f-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="2d36f-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2d36f-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="2d36f-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2d36f-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
