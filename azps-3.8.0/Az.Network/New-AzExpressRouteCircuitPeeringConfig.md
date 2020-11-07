---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c4c3abf1eeb387c700bb456b50887fdc9dd41c74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944749"
---
# <span data-ttu-id="dfba3-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="dfba3-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="dfba3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfba3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfba3-103">Cria uma nova configuração de emparelhamento para ser adicionada a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfba3-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="dfba3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfba3-104">SYNTAX</span></span>

### <span data-ttu-id="dfba3-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfba3-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfba3-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="dfba3-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfba3-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="dfba3-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfba3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfba3-108">DESCRIPTION</span></span>
<span data-ttu-id="dfba3-109">O cmdlet **New-AzExpressRouteCircuitPeeringConfig** adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfba3-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="dfba3-110">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="dfba3-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="dfba3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfba3-111">EXAMPLES</span></span>

### <span data-ttu-id="dfba3-112">Exemplo 1: criar um novo circuito do ExpressRoute com uma configuração de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="dfba3-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="dfba3-113">OS</span><span class="sxs-lookup"><span data-stu-id="dfba3-113">PARAMETERS</span></span>

### <span data-ttu-id="dfba3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfba3-114">-DefaultProfile</span></span>
<span data-ttu-id="dfba3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfba3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfba3-116">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="dfba3-116">-LegacyMode</span></span>
<span data-ttu-id="dfba3-117">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="dfba3-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="dfba3-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="dfba3-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="dfba3-119">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="dfba3-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="dfba3-120">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="dfba3-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="dfba3-121">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="dfba3-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="dfba3-122">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="dfba3-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="dfba3-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="dfba3-124">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="dfba3-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="dfba3-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="dfba3-126">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="dfba3-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfba3-127">-Name</span></span>
<span data-ttu-id="dfba3-128">O nome da configuração de emparelhamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="dfba3-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="dfba3-129">-PeerAddressType</span></span>
<span data-ttu-id="dfba3-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="dfba3-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="dfba3-131">-PeerASN</span></span>
<span data-ttu-id="dfba3-132">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfba3-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="dfba3-133">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="dfba3-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dfba3-134">-PeeringType</span></span>
<span data-ttu-id="dfba3-135">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dfba3-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dfba3-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="dfba3-137">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dfba3-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="dfba3-138">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="dfba3-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="dfba3-139">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="dfba3-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="dfba3-140">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfba3-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="dfba3-141">-RouteFilter</span></span>
<span data-ttu-id="dfba3-142">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="dfba3-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="dfba3-143">-RouteFilterId</span></span>
<span data-ttu-id="dfba3-144">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="dfba3-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dfba3-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="dfba3-146">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dfba3-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="dfba3-147">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="dfba3-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="dfba3-148">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="dfba3-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="dfba3-149">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfba3-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="dfba3-150">-SharedKey</span></span>
<span data-ttu-id="dfba3-151">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dfba3-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-152">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="dfba3-152">-VlanId</span></span>
<span data-ttu-id="dfba3-153">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="dfba3-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfba3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfba3-154">CommonParameters</span></span>
<span data-ttu-id="dfba3-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfba3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfba3-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfba3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfba3-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfba3-157">INPUTS</span></span>

### <span data-ttu-id="dfba3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="dfba3-158">System.String</span></span>

### <span data-ttu-id="dfba3-159">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dfba3-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="dfba3-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfba3-160">System.Boolean</span></span>

## <span data-ttu-id="dfba3-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfba3-161">OUTPUTS</span></span>

### <span data-ttu-id="dfba3-162">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="dfba3-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="dfba3-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfba3-163">NOTES</span></span>

## <span data-ttu-id="dfba3-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfba3-164">RELATED LINKS</span></span>

[<span data-ttu-id="dfba3-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="dfba3-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="dfba3-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dfba3-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="dfba3-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="dfba3-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="dfba3-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dfba3-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
