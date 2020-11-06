---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428051"
---
# <span data-ttu-id="740ec-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="740ec-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="740ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="740ec-102">SYNOPSIS</span></span>
<span data-ttu-id="740ec-103">Remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="740ec-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="740ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="740ec-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="740ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="740ec-105">DESCRIPTION</span></span>
<span data-ttu-id="740ec-106">O cmdlet **Remove-AzureRmLoadBalancerProbeConfig** remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="740ec-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="740ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="740ec-107">EXAMPLES</span></span>

### <span data-ttu-id="740ec-108">Exemplo 1: remover uma configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="740ec-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="740ec-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="740ec-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="740ec-110">O segundo comando exclui a configuração nomeada myprobe do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="740ec-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="740ec-111">OS</span><span class="sxs-lookup"><span data-stu-id="740ec-111">PARAMETERS</span></span>

### <span data-ttu-id="740ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740ec-112">-DefaultProfile</span></span>
<span data-ttu-id="740ec-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="740ec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740ec-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="740ec-114">-LoadBalancer</span></span>
<span data-ttu-id="740ec-115">Especifica o balanceador de carga que contém a configuração de sonda que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="740ec-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="740ec-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="740ec-116">-Name</span></span>
<span data-ttu-id="740ec-117">Especifica o nome da configuração de sondagem que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="740ec-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="740ec-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="740ec-118">-Confirm</span></span>
<span data-ttu-id="740ec-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="740ec-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="740ec-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="740ec-120">-WhatIf</span></span>
<span data-ttu-id="740ec-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="740ec-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="740ec-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="740ec-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="740ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740ec-123">CommonParameters</span></span>
<span data-ttu-id="740ec-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="740ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740ec-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="740ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740ec-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="740ec-126">INPUTS</span></span>

### <span data-ttu-id="740ec-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="740ec-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="740ec-128">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="740ec-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="740ec-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="740ec-129">OUTPUTS</span></span>

### <span data-ttu-id="740ec-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="740ec-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="740ec-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="740ec-131">NOTES</span></span>

## <span data-ttu-id="740ec-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="740ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="740ec-133">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="740ec-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="740ec-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="740ec-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="740ec-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="740ec-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="740ec-136">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="740ec-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="740ec-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="740ec-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

