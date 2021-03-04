---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 23dc75532c7b23c584d586b486e0d67d32af795f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890606"
---
# <span data-ttu-id="174f5-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="174f5-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="174f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="174f5-102">SYNOPSIS</span></span>
<span data-ttu-id="174f5-103">Cria uma nova configuração de peering a ser adicionada a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="174f5-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="174f5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="174f5-104">SYNTAX</span></span>

### <span data-ttu-id="174f5-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="174f5-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="174f5-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="174f5-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="174f5-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="174f5-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="174f5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="174f5-108">DESCRIPTION</span></span>
<span data-ttu-id="174f5-109">O cmdlet **New-AzExpressRouteCircuitPeeringConfig** adiciona uma configuração de peering a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="174f5-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="174f5-110">Os circuitos ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="174f5-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="174f5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="174f5-111">EXAMPLES</span></span>

### <span data-ttu-id="174f5-112">Exemplo 1: Criar um novo circuito ExpressRoute com uma configuração de peering</span><span class="sxs-lookup"><span data-stu-id="174f5-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
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

## <span data-ttu-id="174f5-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="174f5-113">PARAMETERS</span></span>

### <span data-ttu-id="174f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174f5-114">-DefaultProfile</span></span>
<span data-ttu-id="174f5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="174f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="174f5-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="174f5-116">-LegacyMode</span></span>
<span data-ttu-id="174f5-117">O modo herdamento do Peering</span><span class="sxs-lookup"><span data-stu-id="174f5-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="174f5-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="174f5-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="174f5-119">Para um PeeringType do MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que você planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="174f5-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="174f5-120">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="174f5-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="174f5-121">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="174f5-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="174f5-122">Esses prefixos devem ser registrados em um Nome de Registro de Roteamento (RIR/RIR).</span><span class="sxs-lookup"><span data-stu-id="174f5-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="174f5-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="174f5-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="174f5-124">Se você estiver anunciando prefixos que não estão registrados no número AS de paração, você poderá especificar o número AS ao qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="174f5-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="174f5-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="174f5-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="174f5-126">O Nome do Registro de Roteamento (RIR/RIR) ao qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="174f5-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="174f5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="174f5-127">-Name</span></span>
<span data-ttu-id="174f5-128">O nome da configuração de paração a ser criada.</span><span class="sxs-lookup"><span data-stu-id="174f5-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="174f5-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="174f5-129">-PeerAddressType</span></span>
<span data-ttu-id="174f5-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="174f5-130">PeerAddressType</span></span>

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

### <span data-ttu-id="174f5-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="174f5-131">-PeerASN</span></span>
<span data-ttu-id="174f5-132">O número AS do seu circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="174f5-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="174f5-133">Deve ser uma ASN Pública quando PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="174f5-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="174f5-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="174f5-134">-PeeringType</span></span>
<span data-ttu-id="174f5-135">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="174f5-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="174f5-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="174f5-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="174f5-137">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="174f5-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="174f5-138">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="174f5-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="174f5-139">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="174f5-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="174f5-140">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="174f5-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="174f5-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="174f5-141">-RouteFilter</span></span>
<span data-ttu-id="174f5-142">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="174f5-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="174f5-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="174f5-143">-RouteFilterId</span></span>
<span data-ttu-id="174f5-144">Essa é a ID de recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="174f5-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="174f5-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="174f5-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="174f5-146">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="174f5-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="174f5-147">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="174f5-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="174f5-148">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="174f5-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="174f5-149">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="174f5-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="174f5-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="174f5-150">-SharedKey</span></span>
<span data-ttu-id="174f5-151">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="174f5-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="174f5-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="174f5-152">-VlanId</span></span>
<span data-ttu-id="174f5-153">Esse é o número de Id da VLAN atribuída a esse paring.</span><span class="sxs-lookup"><span data-stu-id="174f5-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="174f5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174f5-154">CommonParameters</span></span>
<span data-ttu-id="174f5-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174f5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174f5-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174f5-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174f5-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="174f5-157">INPUTS</span></span>

### <span data-ttu-id="174f5-158">System.String</span><span class="sxs-lookup"><span data-stu-id="174f5-158">System.String</span></span>

### <span data-ttu-id="174f5-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="174f5-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="174f5-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="174f5-160">System.Boolean</span></span>

## <span data-ttu-id="174f5-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="174f5-161">OUTPUTS</span></span>

### <span data-ttu-id="174f5-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="174f5-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="174f5-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="174f5-163">NOTES</span></span>

## <span data-ttu-id="174f5-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="174f5-164">RELATED LINKS</span></span>

[<span data-ttu-id="174f5-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="174f5-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="174f5-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="174f5-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="174f5-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="174f5-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="174f5-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="174f5-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
