---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114687"
---
# <span data-ttu-id="a99d0-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a99d0-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a99d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a99d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a99d0-103">Cria uma nova configuração de peering a ser adicionada a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a99d0-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a99d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a99d0-104">SYNTAX</span></span>

### <span data-ttu-id="a99d0-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a99d0-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a99d0-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="a99d0-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a99d0-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="a99d0-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99d0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a99d0-108">DESCRIPTION</span></span>
<span data-ttu-id="a99d0-109">O **cmdlet New-AzExpressRoute CircuitPeeringConfig** adiciona uma configuração de peering a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a99d0-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="a99d0-110">Os circuitos do ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="a99d0-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="a99d0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a99d0-111">EXAMPLES</span></span>

### <span data-ttu-id="a99d0-112">Exemplo 1: Criar um novo circuito do ExpressRoute com uma configuração de peering</span><span class="sxs-lookup"><span data-stu-id="a99d0-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="a99d0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a99d0-113">PARAMETERS</span></span>

### <span data-ttu-id="a99d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99d0-114">-DefaultProfile</span></span>
<span data-ttu-id="a99d0-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a99d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a99d0-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="a99d0-116">-LegacyMode</span></span>
<span data-ttu-id="a99d0-117">O modo herdário do Peering</span><span class="sxs-lookup"><span data-stu-id="a99d0-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="a99d0-118">-MicrosoftConfigAdvertedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="a99d0-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="a99d0-119">Para um PeeringType da MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="a99d0-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="a99d0-120">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="a99d0-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="a99d0-121">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="a99d0-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="a99d0-122">Esses prefixos devem ser registrados para você em um Nome de Registro de Roteamento (SEMPRE/IRR).</span><span class="sxs-lookup"><span data-stu-id="a99d0-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="a99d0-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="a99d0-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="a99d0-124">Se você estiver anunciando prefixos que não estão registrados no número AS de par, poderá especificar o número AS para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="a99d0-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="a99d0-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="a99d0-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="a99d0-126">O Nome do Registro de Roteamento (NÚM/IRR) para o qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="a99d0-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="a99d0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a99d0-127">-Name</span></span>
<span data-ttu-id="a99d0-128">O nome da configuração de peering a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a99d0-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="a99d0-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a99d0-129">-PeerAddressType</span></span>
<span data-ttu-id="a99d0-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a99d0-130">PeerAddressType</span></span>

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

### <span data-ttu-id="a99d0-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="a99d0-131">-PeerASN</span></span>
<span data-ttu-id="a99d0-132">O número AS do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a99d0-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="a99d0-133">Esse deve ser um ASN Público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="a99d0-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="a99d0-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a99d0-134">-PeeringType</span></span>
<span data-ttu-id="a99d0-135">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a99d0-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a99d0-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a99d0-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="a99d0-137">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de peering.</span><span class="sxs-lookup"><span data-stu-id="a99d0-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="a99d0-138">Essa deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="a99d0-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a99d0-139">O primeiro endereço ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="a99d0-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a99d0-140">O Azure configurará o próximo endereço de número even para a interface de roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="a99d0-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a99d0-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a99d0-141">-RouteFilter</span></span>
<span data-ttu-id="a99d0-142">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="a99d0-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a99d0-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="a99d0-143">-RouteFilterId</span></span>
<span data-ttu-id="a99d0-144">Esta é a ID de recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="a99d0-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a99d0-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a99d0-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="a99d0-146">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de peering.</span><span class="sxs-lookup"><span data-stu-id="a99d0-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="a99d0-147">Essa deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="a99d0-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a99d0-148">O primeiro endereço ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="a99d0-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a99d0-149">O Azure configurará o próximo endereço de número even para a interface de roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="a99d0-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a99d0-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a99d0-150">-SharedKey</span></span>
<span data-ttu-id="a99d0-151">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="a99d0-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="a99d0-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="a99d0-152">-VlanId</span></span>
<span data-ttu-id="a99d0-153">Este é o número de ID da VLAN atribuída para esse peering.</span><span class="sxs-lookup"><span data-stu-id="a99d0-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="a99d0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99d0-154">CommonParameters</span></span>
<span data-ttu-id="a99d0-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99d0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99d0-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99d0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99d0-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="a99d0-157">INPUTS</span></span>

### <span data-ttu-id="a99d0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a99d0-158">System.String</span></span>

### <span data-ttu-id="a99d0-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a99d0-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="a99d0-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a99d0-160">System.Boolean</span></span>

## <span data-ttu-id="a99d0-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="a99d0-161">OUTPUTS</span></span>

### <span data-ttu-id="a99d0-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a99d0-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="a99d0-163">Notas</span><span class="sxs-lookup"><span data-stu-id="a99d0-163">NOTES</span></span>

## <span data-ttu-id="a99d0-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a99d0-164">RELATED LINKS</span></span>

[<span data-ttu-id="a99d0-165">Add-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a99d0-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a99d0-166">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="a99d0-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a99d0-167">Remove-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a99d0-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a99d0-168">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="a99d0-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
