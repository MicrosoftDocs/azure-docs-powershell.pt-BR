---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786436"
---
# <span data-ttu-id="c97f0-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c97f0-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c97f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c97f0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97f0-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c97f0-103">SYNTAX</span></span>

### <span data-ttu-id="c97f0-104">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="c97f0-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97f0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c97f0-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97f0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c97f0-106">DESCRIPTION</span></span>

## <span data-ttu-id="c97f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c97f0-107">EXAMPLES</span></span>

### <span data-ttu-id="c97f0-108">1:</span><span class="sxs-lookup"><span data-stu-id="c97f0-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="c97f0-109">OS</span><span class="sxs-lookup"><span data-stu-id="c97f0-109">PARAMETERS</span></span>

### <span data-ttu-id="c97f0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c97f0-110">-AsJob</span></span>
<span data-ttu-id="c97f0-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c97f0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c97f0-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="c97f0-112">-AuthorizationKey</span></span>
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

### <span data-ttu-id="c97f0-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="c97f0-113">-ConnectionType</span></span>
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

### <span data-ttu-id="c97f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97f0-114">-DefaultProfile</span></span>
<span data-ttu-id="c97f0-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c97f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97f0-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c97f0-116">-EnableBgp</span></span>
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

### <span data-ttu-id="c97f0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c97f0-117">-Force</span></span>
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

### <span data-ttu-id="c97f0-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="c97f0-118">-IpsecPolicies</span></span>
<span data-ttu-id="c97f0-119">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="c97f0-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="c97f0-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="c97f0-120">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="c97f0-121">-Local</span><span class="sxs-lookup"><span data-stu-id="c97f0-121">-Location</span></span>
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

### <span data-ttu-id="c97f0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c97f0-122">-Name</span></span>
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

### <span data-ttu-id="c97f0-123">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="c97f0-123">-Peer</span></span>
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

### <span data-ttu-id="c97f0-124">-Peerid</span><span class="sxs-lookup"><span data-stu-id="c97f0-124">-PeerId</span></span>
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

### <span data-ttu-id="c97f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97f0-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c97f0-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="c97f0-126">-RoutingWeight</span></span>
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

### <span data-ttu-id="c97f0-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c97f0-127">-SharedKey</span></span>
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

### <span data-ttu-id="c97f0-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="c97f0-128">-Tag</span></span>
<span data-ttu-id="c97f0-129">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c97f0-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c97f0-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c97f0-130">For example:</span></span>

<span data-ttu-id="c97f0-131">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c97f0-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c97f0-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c97f0-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c97f0-133">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="c97f0-133">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="c97f0-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="c97f0-134">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="c97f0-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="c97f0-135">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="c97f0-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c97f0-136">-Confirm</span></span>
<span data-ttu-id="c97f0-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c97f0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97f0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97f0-138">-WhatIf</span></span>
<span data-ttu-id="c97f0-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c97f0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97f0-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c97f0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97f0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97f0-141">CommonParameters</span></span>
<span data-ttu-id="c97f0-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97f0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97f0-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97f0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97f0-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c97f0-144">INPUTS</span></span>

## <span data-ttu-id="c97f0-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c97f0-145">OUTPUTS</span></span>

### <span data-ttu-id="c97f0-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c97f0-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c97f0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c97f0-147">NOTES</span></span>

## <span data-ttu-id="c97f0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c97f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="c97f0-149">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c97f0-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c97f0-150">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c97f0-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c97f0-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c97f0-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
