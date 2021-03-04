---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78adeb351c0b18fe8ca7e3c3a2d286abe2f97400
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888616"
---
# <span data-ttu-id="2b61a-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b61a-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2b61a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b61a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b61a-103">Cria a conexão VPN site a site entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="2b61a-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="2b61a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b61a-104">SYNTAX</span></span>

### <span data-ttu-id="2b61a-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b61a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b61a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b61a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b61a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b61a-107">DESCRIPTION</span></span>
<span data-ttu-id="2b61a-108">Cria a conexão VPN site a site entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="2b61a-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="2b61a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b61a-109">EXAMPLES</span></span>

### <span data-ttu-id="2b61a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b61a-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="2b61a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b61a-111">PARAMETERS</span></span>

### <span data-ttu-id="2b61a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b61a-112">-AsJob</span></span>
<span data-ttu-id="2b61a-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2b61a-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="2b61a-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="2b61a-115">-ConnectionProtocol</span></span>
<span data-ttu-id="2b61a-116">Protocolo de conexão de gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="2b61a-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="2b61a-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b61a-118">-DefaultProfile</span></span>
<span data-ttu-id="2b61a-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2b61a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b61a-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2b61a-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="2b61a-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2b61a-122">-Force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="2b61a-123">-IpsecPolicies</span></span>
<span data-ttu-id="2b61a-124">Uma lista de políticas IPSec.</span><span class="sxs-lookup"><span data-stu-id="2b61a-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="2b61a-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-126">-Location</span><span class="sxs-lookup"><span data-stu-id="2b61a-126">-Location</span></span>

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

### <span data-ttu-id="2b61a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2b61a-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="2b61a-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="2b61a-129">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b61a-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="2b61a-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="2b61a-131">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2b61a-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="2b61a-133">Tempo de tempo de detecção de ponto morto da conexão em segundos</span><span class="sxs-lookup"><span data-stu-id="2b61a-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="2b61a-134">-ConnectionMode</span></span>
<span data-ttu-id="2b61a-135">Modo de conexão do Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="2b61a-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2b61a-136">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b61a-137">-Tag</span></span>
<span data-ttu-id="2b61a-138">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2b61a-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b61a-139">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2b61a-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2b61a-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="2b61a-141">Uma lista de políticas de Seletor de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="2b61a-141">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b61a-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="2b61a-143">Se deve usar PrivateIP para este túnel VPN S2S</span><span class="sxs-lookup"><span data-stu-id="2b61a-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="2b61a-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="2b61a-145">Usar seletores de tráfego baseados em política para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="2b61a-145">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="2b61a-146">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="2b61a-147">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b61a-148">-Confirm</span></span>
<span data-ttu-id="2b61a-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b61a-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b61a-150">-WhatIf</span></span>
<span data-ttu-id="2b61a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b61a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b61a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b61a-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b61a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b61a-153">CommonParameters</span></span>
<span data-ttu-id="2b61a-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b61a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b61a-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b61a-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b61a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b61a-156">INPUTS</span></span>

### <span data-ttu-id="2b61a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2b61a-157">System.String</span></span>

### <span data-ttu-id="2b61a-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b61a-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="2b61a-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b61a-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="2b61a-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2b61a-160">System.Int32</span></span>

### <span data-ttu-id="2b61a-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2b61a-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="2b61a-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b61a-162">System.Boolean</span></span>

### <span data-ttu-id="2b61a-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b61a-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2b61a-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="2b61a-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="2b61a-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="2b61a-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="2b61a-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b61a-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b61a-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b61a-167">OUTPUTS</span></span>

### <span data-ttu-id="2b61a-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b61a-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2b61a-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b61a-169">NOTES</span></span>

## <span data-ttu-id="2b61a-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b61a-170">RELATED LINKS</span></span>

[<span data-ttu-id="2b61a-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b61a-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2b61a-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b61a-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2b61a-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2b61a-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
