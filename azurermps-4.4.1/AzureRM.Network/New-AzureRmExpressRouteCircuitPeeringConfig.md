---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7008ec07c4ed8800d5817e6dbf306a1540d89a04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602566"
---
# <span data-ttu-id="c272b-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c272b-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c272b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c272b-102">SYNOPSIS</span></span>
<span data-ttu-id="c272b-103">Cria uma nova configuração de emparelhamento para ser adicionada a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c272b-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c272b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c272b-104">SYNTAX</span></span>

### <span data-ttu-id="c272b-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="c272b-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c272b-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="c272b-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c272b-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="c272b-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c272b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c272b-108">DESCRIPTION</span></span>
<span data-ttu-id="c272b-109">O cmdlet **New-AzureRmExpressRouteCircuitPeeringConfig** adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c272b-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="c272b-110">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="c272b-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="c272b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c272b-111">EXAMPLES</span></span>

### <span data-ttu-id="c272b-112">Exemplo 1: criar um novo circuito do ExpressRoute com uma configuração de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="c272b-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="c272b-113">OS</span><span class="sxs-lookup"><span data-stu-id="c272b-113">PARAMETERS</span></span>

### <span data-ttu-id="c272b-114">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="c272b-114">-LegacyMode</span></span>
<span data-ttu-id="c272b-115">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="c272b-115">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="c272b-116">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="c272b-116">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="c272b-117">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="c272b-117">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="c272b-118">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="c272b-118">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="c272b-119">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="c272b-119">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="c272b-120">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="c272b-120">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c272b-121">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="c272b-121">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="c272b-122">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="c272b-122">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="c272b-123">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="c272b-123">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="c272b-124">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="c272b-124">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="c272b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c272b-125">-Name</span></span>
<span data-ttu-id="c272b-126">O nome da configuração de emparelhamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="c272b-126">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="c272b-127">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c272b-127">-PeerAddressType</span></span>
<span data-ttu-id="c272b-128">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c272b-128">PeerAddressType</span></span>

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

### <span data-ttu-id="c272b-129">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="c272b-129">-PeerASN</span></span>
<span data-ttu-id="c272b-130">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c272b-130">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="c272b-131">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="c272b-131">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="c272b-132">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c272b-132">-PeeringType</span></span>
<span data-ttu-id="c272b-133">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c272b-133">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c272b-134">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c272b-134">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="c272b-135">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="c272b-135">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="c272b-136">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="c272b-136">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c272b-137">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="c272b-137">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c272b-138">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="c272b-138">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c272b-139">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c272b-139">-RouteFilter</span></span>
<span data-ttu-id="c272b-140">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="c272b-140">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c272b-141">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="c272b-141">-RouteFilterId</span></span>
<span data-ttu-id="c272b-142">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="c272b-142">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="c272b-143">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c272b-143">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="c272b-144">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="c272b-144">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="c272b-145">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="c272b-145">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="c272b-146">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="c272b-146">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="c272b-147">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="c272b-147">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="c272b-148">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c272b-148">-SharedKey</span></span>
<span data-ttu-id="c272b-149">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="c272b-149">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="c272b-150">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="c272b-150">-VlanId</span></span>
<span data-ttu-id="c272b-151">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="c272b-151">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="c272b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c272b-152">-DefaultProfile</span></span>
<span data-ttu-id="c272b-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c272b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c272b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c272b-154">CommonParameters</span></span>
<span data-ttu-id="c272b-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c272b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c272b-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c272b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c272b-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c272b-157">INPUTS</span></span>

## <span data-ttu-id="c272b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c272b-158">OUTPUTS</span></span>

### <span data-ttu-id="c272b-159">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c272b-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c272b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c272b-160">NOTES</span></span>

## <span data-ttu-id="c272b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c272b-161">RELATED LINKS</span></span>

[<span data-ttu-id="c272b-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c272b-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c272b-163">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c272b-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c272b-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c272b-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c272b-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c272b-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
