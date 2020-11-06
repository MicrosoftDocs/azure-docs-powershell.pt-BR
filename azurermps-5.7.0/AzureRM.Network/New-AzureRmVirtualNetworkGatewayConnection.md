---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5beb3e7c2c010570089dfd0667eca48e5d1c6728
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609515"
---
# <span data-ttu-id="5fdae-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fdae-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5fdae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fdae-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fdae-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fdae-103">SYNTAX</span></span>

### <span data-ttu-id="5fdae-104">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fdae-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fdae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fdae-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fdae-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fdae-106">DESCRIPTION</span></span>

## <span data-ttu-id="5fdae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fdae-107">EXAMPLES</span></span>

### <span data-ttu-id="5fdae-108">1:</span><span class="sxs-lookup"><span data-stu-id="5fdae-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="5fdae-109">OS</span><span class="sxs-lookup"><span data-stu-id="5fdae-109">PARAMETERS</span></span>

### <span data-ttu-id="5fdae-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fdae-110">-AsJob</span></span>
<span data-ttu-id="5fdae-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fdae-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fdae-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="5fdae-112">-AuthorizationKey</span></span>
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

### <span data-ttu-id="5fdae-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="5fdae-113">-ConnectionType</span></span>
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

### <span data-ttu-id="5fdae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fdae-114">-DefaultProfile</span></span>
<span data-ttu-id="5fdae-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fdae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fdae-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5fdae-116">-EnableBgp</span></span>
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

### <span data-ttu-id="5fdae-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5fdae-117">-Force</span></span>
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

### <span data-ttu-id="5fdae-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="5fdae-118">-IpsecPolicies</span></span>
<span data-ttu-id="5fdae-119">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="5fdae-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="5fdae-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="5fdae-120">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="5fdae-121">-Local</span><span class="sxs-lookup"><span data-stu-id="5fdae-121">-Location</span></span>
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

### <span data-ttu-id="5fdae-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fdae-122">-Name</span></span>
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

### <span data-ttu-id="5fdae-123">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="5fdae-123">-Peer</span></span>
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

### <span data-ttu-id="5fdae-124">-Peerid</span><span class="sxs-lookup"><span data-stu-id="5fdae-124">-PeerId</span></span>
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

### <span data-ttu-id="5fdae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fdae-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5fdae-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="5fdae-126">-RoutingWeight</span></span>
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

### <span data-ttu-id="5fdae-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5fdae-127">-SharedKey</span></span>
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

### <span data-ttu-id="5fdae-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="5fdae-128">-Tag</span></span>
<span data-ttu-id="5fdae-129">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5fdae-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5fdae-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5fdae-130">For example:</span></span>

<span data-ttu-id="5fdae-131">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5fdae-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5fdae-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="5fdae-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="5fdae-133">Usar seletores de tráfego baseado em políticas para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="5fdae-133">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="5fdae-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="5fdae-134">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="5fdae-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="5fdae-135">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="5fdae-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fdae-136">-Confirm</span></span>
<span data-ttu-id="5fdae-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fdae-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fdae-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fdae-138">-WhatIf</span></span>
<span data-ttu-id="5fdae-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fdae-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fdae-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fdae-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fdae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fdae-141">CommonParameters</span></span>
<span data-ttu-id="5fdae-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fdae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fdae-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fdae-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fdae-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fdae-144">INPUTS</span></span>

### <span data-ttu-id="5fdae-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5fdae-145">None</span></span>
<span data-ttu-id="5fdae-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5fdae-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fdae-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fdae-147">OUTPUTS</span></span>

### <span data-ttu-id="5fdae-148">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fdae-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5fdae-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fdae-149">NOTES</span></span>

## <span data-ttu-id="5fdae-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fdae-150">RELATED LINKS</span></span>

[<span data-ttu-id="5fdae-151">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fdae-151">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5fdae-152">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fdae-152">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5fdae-153">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fdae-153">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
