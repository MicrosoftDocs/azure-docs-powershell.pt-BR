---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 7aede18c438faca196d696a69e7f7651edac132e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775350"
---
# <span data-ttu-id="0c34f-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0c34f-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0c34f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c34f-102">SYNOPSIS</span></span>

## <span data-ttu-id="0c34f-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c34f-103">SYNTAX</span></span>

### <span data-ttu-id="0c34f-104">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c34f-104">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c34f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c34f-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c34f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c34f-106">DESCRIPTION</span></span>

## <span data-ttu-id="0c34f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c34f-107">EXAMPLES</span></span>

### <span data-ttu-id="0c34f-108">1:</span><span class="sxs-lookup"><span data-stu-id="0c34f-108">1:</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="0c34f-109">OS</span><span class="sxs-lookup"><span data-stu-id="0c34f-109">PARAMETERS</span></span>

### <span data-ttu-id="0c34f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c34f-110">-AsJob</span></span>
<span data-ttu-id="0c34f-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c34f-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0c34f-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="0c34f-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c34f-114">-DefaultProfile</span></span>
<span data-ttu-id="0c34f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c34f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0c34f-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0c34f-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="0c34f-118">-IpsecPolicies</span></span>
<span data-ttu-id="0c34f-119">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="0c34f-119">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="0c34f-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="0c34f-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c34f-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-123">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="0c34f-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-124">-Peerid</span><span class="sxs-lookup"><span data-stu-id="0c34f-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c34f-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="0c34f-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="0c34f-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="0c34f-128">-Tag</span></span>
<span data-ttu-id="0c34f-129">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0c34f-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c34f-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0c34f-130">For example:</span></span>

<span data-ttu-id="0c34f-131">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0c34f-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="0c34f-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="0c34f-133">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="0c34f-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="0c34f-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="0c34f-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c34f-136">-Confirm</span></span>
<span data-ttu-id="0c34f-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c34f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c34f-138">-WhatIf</span></span>
<span data-ttu-id="0c34f-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c34f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c34f-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c34f-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c34f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c34f-141">CommonParameters</span></span>
<span data-ttu-id="0c34f-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c34f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c34f-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c34f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c34f-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c34f-144">INPUTS</span></span>

## <span data-ttu-id="0c34f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c34f-145">OUTPUTS</span></span>

### <span data-ttu-id="0c34f-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0c34f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0c34f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c34f-147">NOTES</span></span>

## <span data-ttu-id="0c34f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c34f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0c34f-149">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0c34f-149">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0c34f-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0c34f-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0c34f-151">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0c34f-151">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
