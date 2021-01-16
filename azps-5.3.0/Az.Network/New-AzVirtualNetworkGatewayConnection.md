---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429546"
---
# <span data-ttu-id="f44f4-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f44f4-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f44f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f44f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f44f4-103">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="f44f4-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f44f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f44f4-104">SYNTAX</span></span>

### <span data-ttu-id="f44f4-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f44f4-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f44f4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f44f4-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f44f4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f44f4-107">DESCRIPTION</span></span>
<span data-ttu-id="f44f4-108">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="f44f4-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f44f4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f44f4-109">EXAMPLES</span></span>

### <span data-ttu-id="f44f4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f44f4-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="f44f4-111">OS</span><span class="sxs-lookup"><span data-stu-id="f44f4-111">PARAMETERS</span></span>

### <span data-ttu-id="f44f4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f44f4-112">-AsJob</span></span>
<span data-ttu-id="f44f4-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f44f4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f44f4-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f44f4-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="f44f4-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="f44f4-115">-ConnectionProtocol</span></span>
<span data-ttu-id="f44f4-116">Protocolo de conexão de gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="f44f4-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="f44f4-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="f44f4-117">-ConnectionType</span></span>

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

### <span data-ttu-id="f44f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44f4-118">-DefaultProfile</span></span>
<span data-ttu-id="f44f4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f44f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f44f4-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f44f4-120">-EnableBgp</span></span>

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

### <span data-ttu-id="f44f4-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="f44f4-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="f44f4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f44f4-122">-Force</span></span>

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

### <span data-ttu-id="f44f4-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="f44f4-123">-IpsecPolicies</span></span>
<span data-ttu-id="f44f4-124">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="f44f4-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="f44f4-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f44f4-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="f44f4-126">-Local</span><span class="sxs-lookup"><span data-stu-id="f44f4-126">-Location</span></span>

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

### <span data-ttu-id="f44f4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f44f4-127">-Name</span></span>

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

### <span data-ttu-id="f44f4-128">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="f44f4-128">-Peer</span></span>

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

### <span data-ttu-id="f44f4-129">-Peerid</span><span class="sxs-lookup"><span data-stu-id="f44f4-129">-PeerId</span></span>

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

### <span data-ttu-id="f44f4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f44f4-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="f44f4-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="f44f4-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="f44f4-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="f44f4-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="f44f4-133">Tempo limite de detecção de par inativo da conexão em segundos</span><span class="sxs-lookup"><span data-stu-id="f44f4-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="f44f4-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f44f4-134">-SharedKey</span></span>

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

### <span data-ttu-id="f44f4-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="f44f4-135">-Tag</span></span>
<span data-ttu-id="f44f4-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f44f4-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f44f4-137">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f44f4-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f44f4-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f44f4-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="f44f4-139">Uma lista de políticas do seletor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f44f4-139">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="f44f4-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="f44f4-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="f44f4-141">Se o PrivateIP deve ser usado para esse encapsulamento VPN S2S</span><span class="sxs-lookup"><span data-stu-id="f44f4-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="f44f4-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f44f4-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f44f4-143">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="f44f4-143">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="f44f4-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="f44f4-144">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="f44f4-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f44f4-145">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="f44f4-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f44f4-146">-Confirm</span></span>
<span data-ttu-id="f44f4-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f44f4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f44f4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f44f4-148">-WhatIf</span></span>
<span data-ttu-id="f44f4-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f44f4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f44f4-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f44f4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f44f4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44f4-151">CommonParameters</span></span>
<span data-ttu-id="f44f4-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f44f4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44f4-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44f4-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44f4-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f44f4-154">INPUTS</span></span>

### <span data-ttu-id="f44f4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f44f4-155">System.String</span></span>

### <span data-ttu-id="f44f4-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f44f4-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f44f4-157">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f44f4-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f44f4-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f44f4-158">System.Int32</span></span>

### <span data-ttu-id="f44f4-159">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f44f4-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="f44f4-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f44f4-160">System.Boolean</span></span>

### <span data-ttu-id="f44f4-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f44f4-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f44f4-162">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f44f4-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f44f4-163">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="f44f4-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="f44f4-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f44f4-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f44f4-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f44f4-165">OUTPUTS</span></span>

### <span data-ttu-id="f44f4-166">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f44f4-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f44f4-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f44f4-167">NOTES</span></span>

## <span data-ttu-id="f44f4-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f44f4-168">RELATED LINKS</span></span>

[<span data-ttu-id="f44f4-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f44f4-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f44f4-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f44f4-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f44f4-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f44f4-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
