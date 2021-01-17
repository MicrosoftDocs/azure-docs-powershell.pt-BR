---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428911"
---
# <span data-ttu-id="f6f02-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6f02-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f6f02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6f02-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f02-103">Remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6f02-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="f6f02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6f02-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6f02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6f02-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f02-106">O cmdlet **Remove-AzLoadBalancerProbeConfig** remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6f02-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="f6f02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6f02-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f02-108">Exemplo 1: remover uma configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f6f02-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f6f02-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f6f02-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="f6f02-110">O segundo comando exclui a configuração nomeada myprobe do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f6f02-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f6f02-111">OS</span><span class="sxs-lookup"><span data-stu-id="f6f02-111">PARAMETERS</span></span>

### <span data-ttu-id="f6f02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f02-112">-DefaultProfile</span></span>
<span data-ttu-id="f6f02-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f02-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f6f02-114">-LoadBalancer</span></span>
<span data-ttu-id="f6f02-115">Especifica o balanceador de carga que contém a configuração de sonda que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f6f02-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6f02-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6f02-116">-Name</span></span>
<span data-ttu-id="f6f02-117">Especifica o nome da configuração de sondagem que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f6f02-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6f02-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6f02-118">-Confirm</span></span>
<span data-ttu-id="f6f02-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6f02-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f02-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f02-120">-WhatIf</span></span>
<span data-ttu-id="f6f02-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6f02-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6f02-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6f02-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f02-123">CommonParameters</span></span>
<span data-ttu-id="f6f02-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f02-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f02-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f02-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6f02-126">INPUTS</span></span>

### <span data-ttu-id="f6f02-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6f02-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f6f02-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6f02-128">OUTPUTS</span></span>

### <span data-ttu-id="f6f02-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6f02-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f6f02-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6f02-130">NOTES</span></span>

## <span data-ttu-id="f6f02-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6f02-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6f02-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6f02-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6f02-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6f02-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f6f02-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6f02-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6f02-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6f02-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f6f02-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f6f02-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


