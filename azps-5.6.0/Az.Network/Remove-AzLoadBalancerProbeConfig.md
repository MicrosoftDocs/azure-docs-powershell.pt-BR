---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890760"
---
# <span data-ttu-id="ddaff-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ddaff-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ddaff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddaff-102">SYNOPSIS</span></span>
<span data-ttu-id="ddaff-103">Remove uma configuração de sonda de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ddaff-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ddaff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddaff-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddaff-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddaff-105">DESCRIPTION</span></span>
<span data-ttu-id="ddaff-106">O cmdlet **Remove-AzLoadBalancerProbeConfig** remove uma configuração de sonda de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ddaff-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ddaff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddaff-107">EXAMPLES</span></span>

### <span data-ttu-id="ddaff-108">Exemplo 1: Remover uma configuração de sonda de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ddaff-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ddaff-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $loadbalancer de carga.</span><span class="sxs-lookup"><span data-stu-id="ddaff-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="ddaff-110">O segundo comando exclui a configuração chamada MyProbe do balanceador de carga no $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="ddaff-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ddaff-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddaff-111">PARAMETERS</span></span>

### <span data-ttu-id="ddaff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddaff-112">-DefaultProfile</span></span>
<span data-ttu-id="ddaff-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ddaff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddaff-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddaff-114">-LoadBalancer</span></span>
<span data-ttu-id="ddaff-115">Especifica o balanceador de carga que contém a configuração da sonda que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="ddaff-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddaff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ddaff-116">-Name</span></span>
<span data-ttu-id="ddaff-117">Especifica o nome da configuração da sonda que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="ddaff-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddaff-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddaff-118">-Confirm</span></span>
<span data-ttu-id="ddaff-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddaff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddaff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddaff-120">-WhatIf</span></span>
<span data-ttu-id="ddaff-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddaff-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddaff-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddaff-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddaff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddaff-123">CommonParameters</span></span>
<span data-ttu-id="ddaff-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddaff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddaff-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddaff-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddaff-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddaff-126">INPUTS</span></span>

### <span data-ttu-id="ddaff-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddaff-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ddaff-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddaff-128">OUTPUTS</span></span>

### <span data-ttu-id="ddaff-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddaff-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ddaff-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddaff-130">NOTES</span></span>

## <span data-ttu-id="ddaff-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddaff-131">RELATED LINKS</span></span>

[<span data-ttu-id="ddaff-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ddaff-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ddaff-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ddaff-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ddaff-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ddaff-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ddaff-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ddaff-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ddaff-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ddaff-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


