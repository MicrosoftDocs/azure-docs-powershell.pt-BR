---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115088"
---
# <span data-ttu-id="e9e91-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9e91-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e9e91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9e91-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e91-103">Remove uma configuração de configuração de configuração de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e9e91-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e9e91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9e91-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e91-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9e91-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e91-106">O cmdlet **Remove-AzLoadBalancerProbeConfig** remove uma configuração de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e9e91-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e9e91-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9e91-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e91-108">Exemplo 1: Remover uma configuração de configuração de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="e9e91-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e9e91-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $loadbalancer dados.</span><span class="sxs-lookup"><span data-stu-id="e9e91-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="e9e91-110">O segundo comando exclui a configuração chamada MyProbe do balanceador de carga no $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e9e91-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e9e91-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9e91-111">PARAMETERS</span></span>

### <span data-ttu-id="e9e91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e91-112">-DefaultProfile</span></span>
<span data-ttu-id="e9e91-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e9e91-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9e91-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9e91-114">-LoadBalancer</span></span>
<span data-ttu-id="e9e91-115">Especifica o balanceador de carga que contém a configuração de configuração que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e9e91-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9e91-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9e91-116">-Name</span></span>
<span data-ttu-id="e9e91-117">Especifica o nome da configuração de configuração que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e9e91-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9e91-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e9e91-118">-Confirm</span></span>
<span data-ttu-id="e9e91-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e91-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e91-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e91-120">-WhatIf</span></span>
<span data-ttu-id="e9e91-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e9e91-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9e91-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9e91-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e91-123">CommonParameters</span></span>
<span data-ttu-id="e9e91-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e91-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e91-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e91-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9e91-126">INPUTS</span></span>

### <span data-ttu-id="e9e91-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9e91-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e9e91-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9e91-128">OUTPUTS</span></span>

### <span data-ttu-id="e9e91-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9e91-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e9e91-130">Notas</span><span class="sxs-lookup"><span data-stu-id="e9e91-130">NOTES</span></span>

## <span data-ttu-id="e9e91-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9e91-131">RELATED LINKS</span></span>

[<span data-ttu-id="e9e91-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9e91-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9e91-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e9e91-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e9e91-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9e91-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9e91-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9e91-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9e91-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9e91-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


