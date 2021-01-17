---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428952"
---
# <span data-ttu-id="b9b4c-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="b9b4c-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="b9b4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b4c-103">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="b9b4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9b4c-104">SYNTAX</span></span>

### <span data-ttu-id="b9b4c-105">SetByResourcePublicIpAddress (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9b4c-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b4c-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9b4c-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b4c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b4c-108">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="b9b4c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="b9b4c-110">Exemplo 1: nova configuração de endereço de loadbalancer com referência de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b9b4c-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="b9b4c-111">Exemplo 2: nova configuração de endereço de loadbalancer com referência de configuração de IP de front-end de metaequilíbrios</span><span class="sxs-lookup"><span data-stu-id="b9b4c-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="b9b4c-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="b9b4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b4c-113">-DefaultProfile</span></span>
<span data-ttu-id="b9b4c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b4c-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b9b4c-115">-IpAddress</span></span>
<span data-ttu-id="b9b4c-116">O IPAddress a ser adicionado ao pool de back-end</span><span class="sxs-lookup"><span data-stu-id="b9b4c-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="b9b4c-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b9b4c-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="b9b4c-118">A configuração de IP de front-end de balanceamento de carga associada ao config</span><span class="sxs-lookup"><span data-stu-id="b9b4c-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="b9b4c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9b4c-119">-Name</span></span>
<span data-ttu-id="b9b4c-120">O nome da configuração do endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="b9b4c-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="b9b4c-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b9b4c-121">-VirtualNetworkId</span></span>
<span data-ttu-id="b9b4c-122">A rede virtual associada à configuração de endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="b9b4c-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="b9b4c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9b4c-123">-Confirm</span></span>
<span data-ttu-id="b9b4c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b4c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b4c-125">-WhatIf</span></span>
<span data-ttu-id="b9b4c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9b4c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b4c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b4c-128">CommonParameters</span></span>
<span data-ttu-id="b9b4c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b4c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b4c-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9b4c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b4c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9b4c-131">INPUTS</span></span>

### <span data-ttu-id="b9b4c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9b4c-132">System.String</span></span>

### <span data-ttu-id="b9b4c-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b9b4c-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b9b4c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9b4c-134">OUTPUTS</span></span>

### <span data-ttu-id="b9b4c-135">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b9b4c-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="b9b4c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9b4c-136">NOTES</span></span>

## <span data-ttu-id="b9b4c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9b4c-137">RELATED LINKS</span></span>
