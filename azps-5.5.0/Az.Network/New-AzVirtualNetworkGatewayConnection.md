---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 120e20eb62b5475a587a3d272e84c7af1e40cd45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117376"
---
# <span data-ttu-id="084c5-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="084c5-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="084c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="084c5-102">SYNOPSIS</span></span>
<span data-ttu-id="084c5-103">Cria a conexão VPN de Site para Site entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="084c5-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="084c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="084c5-104">SYNTAX</span></span>

### <span data-ttu-id="084c5-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="084c5-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="084c5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="084c5-106">SetByResourceId</span></span>
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

## <span data-ttu-id="084c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="084c5-107">DESCRIPTION</span></span>
<span data-ttu-id="084c5-108">Cria a conexão VPN de Site para Site entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="084c5-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="084c5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="084c5-109">EXAMPLES</span></span>

### <span data-ttu-id="084c5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="084c5-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="084c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="084c5-111">PARAMETERS</span></span>

### <span data-ttu-id="084c5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="084c5-112">-AsJob</span></span>
<span data-ttu-id="084c5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="084c5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="084c5-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="084c5-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="084c5-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="084c5-115">-ConnectionProtocol</span></span>
<span data-ttu-id="084c5-116">Protocolo de conexão do gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="084c5-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="084c5-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="084c5-117">-ConnectionType</span></span>

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

### <span data-ttu-id="084c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084c5-118">-DefaultProfile</span></span>
<span data-ttu-id="084c5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="084c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="084c5-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="084c5-120">-EnableBgp</span></span>

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

### <span data-ttu-id="084c5-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="084c5-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="084c5-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="084c5-122">-Force</span></span>

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

### <span data-ttu-id="084c5-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="084c5-123">-IpsecPolicies</span></span>
<span data-ttu-id="084c5-124">Uma lista de políticas IPSec.</span><span class="sxs-lookup"><span data-stu-id="084c5-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="084c5-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="084c5-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="084c5-126">-Local</span><span class="sxs-lookup"><span data-stu-id="084c5-126">-Location</span></span>

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

### <span data-ttu-id="084c5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="084c5-127">-Name</span></span>

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

### <span data-ttu-id="084c5-128">-Ponto</span><span class="sxs-lookup"><span data-stu-id="084c5-128">-Peer</span></span>

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

### <span data-ttu-id="084c5-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="084c5-129">-PeerId</span></span>

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

### <span data-ttu-id="084c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084c5-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="084c5-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="084c5-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="084c5-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="084c5-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="084c5-133">Tempo de Tempo De detecção de ponto morto da conexão em segundos</span><span class="sxs-lookup"><span data-stu-id="084c5-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="084c5-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="084c5-134">-ConnectionMode</span></span>
<span data-ttu-id="084c5-135">Modo de Conexão do Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="084c5-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="084c5-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="084c5-136">-SharedKey</span></span>

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

### <span data-ttu-id="084c5-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="084c5-137">-Tag</span></span>
<span data-ttu-id="084c5-138">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="084c5-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="084c5-139">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="084c5-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="084c5-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="084c5-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="084c5-141">Uma lista de políticas do Seletor de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="084c5-141">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="084c5-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="084c5-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="084c5-143">Se você quer usar o PrivateIP para este túnel S2S VPN</span><span class="sxs-lookup"><span data-stu-id="084c5-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="084c5-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="084c5-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="084c5-145">Usar seletores de tráfego baseados em política para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="084c5-145">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="084c5-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="084c5-146">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="084c5-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="084c5-147">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="084c5-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="084c5-148">-Confirm</span></span>
<span data-ttu-id="084c5-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084c5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084c5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084c5-150">-WhatIf</span></span>
<span data-ttu-id="084c5-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="084c5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084c5-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="084c5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084c5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084c5-153">CommonParameters</span></span>
<span data-ttu-id="084c5-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084c5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084c5-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084c5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084c5-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="084c5-156">INPUTS</span></span>

### <span data-ttu-id="084c5-157">System.String</span><span class="sxs-lookup"><span data-stu-id="084c5-157">System.String</span></span>

### <span data-ttu-id="084c5-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="084c5-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="084c5-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="084c5-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="084c5-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="084c5-160">System.Int32</span></span>

### <span data-ttu-id="084c5-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="084c5-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="084c5-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="084c5-162">System.Boolean</span></span>

### <span data-ttu-id="084c5-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="084c5-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="084c5-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="084c5-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="084c5-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="084c5-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="084c5-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="084c5-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="084c5-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="084c5-167">OUTPUTS</span></span>

### <span data-ttu-id="084c5-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="084c5-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="084c5-169">Notas</span><span class="sxs-lookup"><span data-stu-id="084c5-169">NOTES</span></span>

## <span data-ttu-id="084c5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="084c5-170">RELATED LINKS</span></span>

[<span data-ttu-id="084c5-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="084c5-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="084c5-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="084c5-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="084c5-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="084c5-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
