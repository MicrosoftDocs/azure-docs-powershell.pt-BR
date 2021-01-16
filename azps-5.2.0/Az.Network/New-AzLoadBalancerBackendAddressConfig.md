---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259600"
---
# <span data-ttu-id="c4d57-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="c4d57-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="c4d57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4d57-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d57-103">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c4d57-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="c4d57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4d57-104">SYNTAX</span></span>

### <span data-ttu-id="c4d57-105">SetByResourcePublicIpAddress (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4d57-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d57-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4d57-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4d57-107">DESCRIPTION</span></span>
<span data-ttu-id="c4d57-108">Retorna uma configuração de endereço back-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c4d57-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="c4d57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4d57-109">EXAMPLES</span></span>

### <span data-ttu-id="c4d57-110">Exemplo 1: nova configuração de endereço de loadbalancer com referência de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4d57-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="c4d57-111">Exemplo 2: nova configuração de endereço de loadbalancer com referência de configuração de IP de front-end de metaequilíbrios</span><span class="sxs-lookup"><span data-stu-id="c4d57-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="c4d57-112">OS</span><span class="sxs-lookup"><span data-stu-id="c4d57-112">PARAMETERS</span></span>

### <span data-ttu-id="c4d57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d57-113">-DefaultProfile</span></span>
<span data-ttu-id="c4d57-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d57-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c4d57-115">-IpAddress</span></span>
<span data-ttu-id="c4d57-116">O IPAddress a ser adicionado ao pool de back-end</span><span class="sxs-lookup"><span data-stu-id="c4d57-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="c4d57-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c4d57-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="c4d57-118">A configuração de IP de front-end de balanceamento de carga associada ao config</span><span class="sxs-lookup"><span data-stu-id="c4d57-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="c4d57-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4d57-119">-Name</span></span>
<span data-ttu-id="c4d57-120">O nome da configuração do endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="c4d57-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="c4d57-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c4d57-121">-VirtualNetworkId</span></span>
<span data-ttu-id="c4d57-122">A rede virtual associada à configuração de endereço de back-end</span><span class="sxs-lookup"><span data-stu-id="c4d57-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="c4d57-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4d57-123">-Confirm</span></span>
<span data-ttu-id="c4d57-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d57-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d57-125">-WhatIf</span></span>
<span data-ttu-id="c4d57-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4d57-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4d57-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4d57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d57-128">CommonParameters</span></span>
<span data-ttu-id="c4d57-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d57-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4d57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d57-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4d57-131">INPUTS</span></span>

### <span data-ttu-id="c4d57-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d57-132">System.String</span></span>

### <span data-ttu-id="c4d57-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4d57-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c4d57-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4d57-134">OUTPUTS</span></span>

### <span data-ttu-id="c4d57-135">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c4d57-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="c4d57-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4d57-136">NOTES</span></span>

## <span data-ttu-id="c4d57-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4d57-137">RELATED LINKS</span></span>
