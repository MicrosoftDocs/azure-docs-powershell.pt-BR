---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c25b311a4f99814c718ce825d61433d7c2fee192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772334"
---
# <span data-ttu-id="7ac99-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ac99-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7ac99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ac99-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac99-103">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="7ac99-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="7ac99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ac99-104">SYNTAX</span></span>

### <span data-ttu-id="7ac99-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ac99-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac99-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac99-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ac99-107">DESCRIPTION</span></span>
<span data-ttu-id="7ac99-108">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="7ac99-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="7ac99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ac99-109">EXAMPLES</span></span>

### <span data-ttu-id="7ac99-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ac99-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="7ac99-111">OS</span><span class="sxs-lookup"><span data-stu-id="7ac99-111">PARAMETERS</span></span>

### <span data-ttu-id="7ac99-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac99-112">-AsJob</span></span>
<span data-ttu-id="7ac99-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7ac99-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ac99-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7ac99-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="7ac99-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="7ac99-115">-ConnectionProtocol</span></span>
<span data-ttu-id="7ac99-116">Protocolo de conexão de gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="7ac99-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="7ac99-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="7ac99-117">-ConnectionType</span></span>

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

### <span data-ttu-id="7ac99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac99-118">-DefaultProfile</span></span>
<span data-ttu-id="7ac99-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac99-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac99-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7ac99-120">-EnableBgp</span></span>

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

### <span data-ttu-id="7ac99-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="7ac99-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="7ac99-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7ac99-122">-Force</span></span>

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

### <span data-ttu-id="7ac99-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="7ac99-123">-IpsecPolicies</span></span>
<span data-ttu-id="7ac99-124">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="7ac99-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="7ac99-125">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac99-125">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="7ac99-126">Uma lista de políticas do seletor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="7ac99-126">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="7ac99-127">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7ac99-127">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="7ac99-128">-Local</span><span class="sxs-lookup"><span data-stu-id="7ac99-128">-Location</span></span>

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

### <span data-ttu-id="7ac99-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ac99-129">-Name</span></span>

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

### <span data-ttu-id="7ac99-130">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="7ac99-130">-Peer</span></span>

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

### <span data-ttu-id="7ac99-131">-Peerid</span><span class="sxs-lookup"><span data-stu-id="7ac99-131">-PeerId</span></span>

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

### <span data-ttu-id="7ac99-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac99-132">-ResourceGroupName</span></span>

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

### <span data-ttu-id="7ac99-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7ac99-133">-RoutingWeight</span></span>

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

### <span data-ttu-id="7ac99-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7ac99-134">-SharedKey</span></span>

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

### <span data-ttu-id="7ac99-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="7ac99-135">-Tag</span></span>
<span data-ttu-id="7ac99-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7ac99-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7ac99-137">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7ac99-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7ac99-138">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7ac99-138">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7ac99-139">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="7ac99-139">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="7ac99-140">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="7ac99-140">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="7ac99-141">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7ac99-141">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="7ac99-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ac99-142">-Confirm</span></span>
<span data-ttu-id="7ac99-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac99-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac99-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac99-144">-WhatIf</span></span>
<span data-ttu-id="7ac99-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ac99-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac99-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ac99-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac99-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac99-147">CommonParameters</span></span>
<span data-ttu-id="7ac99-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac99-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac99-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac99-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac99-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ac99-150">INPUTS</span></span>

### <span data-ttu-id="7ac99-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac99-151">System.String</span></span>

### <span data-ttu-id="7ac99-152">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ac99-152">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7ac99-153">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7ac99-153">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7ac99-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ac99-154">System.Int32</span></span>

### <span data-ttu-id="7ac99-155">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7ac99-155">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="7ac99-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ac99-156">System.Boolean</span></span>

### <span data-ttu-id="7ac99-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ac99-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ac99-158">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7ac99-158">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7ac99-159">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="7ac99-159">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="7ac99-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ac99-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ac99-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ac99-161">OUTPUTS</span></span>

### <span data-ttu-id="7ac99-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ac99-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7ac99-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ac99-163">NOTES</span></span>

## <span data-ttu-id="7ac99-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ac99-164">RELATED LINKS</span></span>

[<span data-ttu-id="7ac99-165">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ac99-165">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7ac99-166">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ac99-166">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7ac99-167">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ac99-167">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
