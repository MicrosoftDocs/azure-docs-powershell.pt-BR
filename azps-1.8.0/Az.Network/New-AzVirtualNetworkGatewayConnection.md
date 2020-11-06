---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600260"
---
# <span data-ttu-id="3f89c-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f89c-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3f89c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f89c-103">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="3f89c-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="3f89c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f89c-104">SYNTAX</span></span>

### <span data-ttu-id="3f89c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f89c-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f89c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f89c-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f89c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f89c-107">DESCRIPTION</span></span>
<span data-ttu-id="3f89c-108">Cria a conexão VPN entre sites entre o gateway de rede virtual e o dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="3f89c-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="3f89c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f89c-109">EXAMPLES</span></span>

### <span data-ttu-id="3f89c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f89c-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="3f89c-111">OS</span><span class="sxs-lookup"><span data-stu-id="3f89c-111">PARAMETERS</span></span>

### <span data-ttu-id="3f89c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f89c-112">-AsJob</span></span>
<span data-ttu-id="3f89c-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3f89c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f89c-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="3f89c-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="3f89c-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="3f89c-115">-ConnectionType</span></span>

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

### <span data-ttu-id="3f89c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f89c-116">-DefaultProfile</span></span>
<span data-ttu-id="3f89c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f89c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f89c-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3f89c-118">-EnableBgp</span></span>

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

### <span data-ttu-id="3f89c-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="3f89c-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="3f89c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3f89c-120">-Force</span></span>

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

### <span data-ttu-id="3f89c-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="3f89c-121">-IpsecPolicies</span></span>
<span data-ttu-id="3f89c-122">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="3f89c-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="3f89c-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="3f89c-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="3f89c-124">-Local</span><span class="sxs-lookup"><span data-stu-id="3f89c-124">-Location</span></span>

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

### <span data-ttu-id="3f89c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f89c-125">-Name</span></span>

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

### <span data-ttu-id="3f89c-126">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="3f89c-126">-Peer</span></span>

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

### <span data-ttu-id="3f89c-127">-Peerid</span><span class="sxs-lookup"><span data-stu-id="3f89c-127">-PeerId</span></span>

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

### <span data-ttu-id="3f89c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f89c-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="3f89c-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="3f89c-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="3f89c-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3f89c-130">-SharedKey</span></span>

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

### <span data-ttu-id="3f89c-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="3f89c-131">-Tag</span></span>
<span data-ttu-id="3f89c-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3f89c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f89c-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3f89c-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f89c-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="3f89c-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="3f89c-135">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="3f89c-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="3f89c-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="3f89c-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="3f89c-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="3f89c-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="3f89c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f89c-138">-Confirm</span></span>
<span data-ttu-id="3f89c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f89c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f89c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f89c-140">-WhatIf</span></span>
<span data-ttu-id="3f89c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f89c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f89c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f89c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f89c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f89c-143">CommonParameters</span></span>
<span data-ttu-id="3f89c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f89c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f89c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f89c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f89c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f89c-146">INPUTS</span></span>

### <span data-ttu-id="3f89c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3f89c-147">System.String</span></span>

### <span data-ttu-id="3f89c-148">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f89c-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3f89c-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f89c-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="3f89c-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3f89c-150">System.Int32</span></span>

### <span data-ttu-id="3f89c-151">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="3f89c-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="3f89c-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f89c-152">System.Boolean</span></span>

### <span data-ttu-id="3f89c-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3f89c-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3f89c-154">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="3f89c-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="3f89c-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f89c-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f89c-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f89c-156">OUTPUTS</span></span>

### <span data-ttu-id="3f89c-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f89c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3f89c-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f89c-158">NOTES</span></span>

## <span data-ttu-id="3f89c-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f89c-159">RELATED LINKS</span></span>

[<span data-ttu-id="3f89c-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f89c-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3f89c-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f89c-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3f89c-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f89c-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
