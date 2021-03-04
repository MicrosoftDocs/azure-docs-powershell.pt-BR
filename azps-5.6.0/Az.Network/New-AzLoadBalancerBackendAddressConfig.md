---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 980b16d373f17101266908c0a24443764d96561f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885861"
---
# <span data-ttu-id="de760-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="de760-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="de760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de760-102">SYNOPSIS</span></span>
<span data-ttu-id="de760-103">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de760-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="de760-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de760-104">SYNTAX</span></span>

### <span data-ttu-id="de760-105">SetByResourcePublicIpAddress (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de760-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de760-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de760-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de760-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de760-107">DESCRIPTION</span></span>
<span data-ttu-id="de760-108">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de760-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="de760-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de760-109">EXAMPLES</span></span>

### <span data-ttu-id="de760-110">Exemplo 1: Nova configuração de endereço do loadbalancer com referência de rede virtual</span><span class="sxs-lookup"><span data-stu-id="de760-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="de760-111">Exemplo 2: Nova configuração de endereço do loadbalancer com referência de configuração ip frontend do loadbalancer</span><span class="sxs-lookup"><span data-stu-id="de760-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="de760-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de760-112">PARAMETERS</span></span>

### <span data-ttu-id="de760-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de760-113">-DefaultProfile</span></span>
<span data-ttu-id="de760-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de760-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de760-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="de760-115">-IpAddress</span></span>
<span data-ttu-id="de760-116">O IPAddress a ser adicionar ao pool de back-end</span><span class="sxs-lookup"><span data-stu-id="de760-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de760-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de760-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="de760-118">A configuração de ip frontend do balanceador de carga associada à configuração de endereço back-end</span><span class="sxs-lookup"><span data-stu-id="de760-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de760-119">-Name</span><span class="sxs-lookup"><span data-stu-id="de760-119">-Name</span></span>
<span data-ttu-id="de760-120">O nome da configuração endereço back-end</span><span class="sxs-lookup"><span data-stu-id="de760-120">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de760-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="de760-121">-VirtualNetworkId</span></span>
<span data-ttu-id="de760-122">A rede virtual associada à configuração endereço back-end</span><span class="sxs-lookup"><span data-stu-id="de760-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de760-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de760-123">-Confirm</span></span>
<span data-ttu-id="de760-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de760-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de760-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de760-125">-WhatIf</span></span>
<span data-ttu-id="de760-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de760-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de760-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de760-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de760-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de760-128">CommonParameters</span></span>
<span data-ttu-id="de760-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de760-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de760-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de760-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de760-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de760-131">INPUTS</span></span>

### <span data-ttu-id="de760-132">System.String</span><span class="sxs-lookup"><span data-stu-id="de760-132">System.String</span></span>

### <span data-ttu-id="de760-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="de760-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="de760-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de760-134">OUTPUTS</span></span>

### <span data-ttu-id="de760-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="de760-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="de760-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="de760-136">NOTES</span></span>

## <span data-ttu-id="de760-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de760-137">RELATED LINKS</span></span>
