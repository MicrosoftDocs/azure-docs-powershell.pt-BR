---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4c1205599f048e33534f0ce0aa844da7b428b076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893143"
---
# <span data-ttu-id="17882-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="17882-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="17882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17882-102">SYNOPSIS</span></span>
<span data-ttu-id="17882-103">Adiciona uma configuração de peering a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17882-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="17882-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17882-104">SYNTAX</span></span>

### <span data-ttu-id="17882-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17882-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17882-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="17882-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17882-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="17882-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17882-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17882-108">DESCRIPTION</span></span>
<span data-ttu-id="17882-109">O cmdlet **Add-AzExpressRouteCircuitPeeringConfig** adiciona uma configuração de peering a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17882-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="17882-110">Os circuitos ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="17882-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="17882-111">Observe que, após executar **Add-AzExpressRouteCircuitPeeringConfig,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="17882-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="17882-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17882-112">EXAMPLES</span></span>

### <span data-ttu-id="17882-113">Exemplo 1: Adicionar um par a um circuito ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="17882-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="17882-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17882-114">PARAMETERS</span></span>

### <span data-ttu-id="17882-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17882-115">-DefaultProfile</span></span>
<span data-ttu-id="17882-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="17882-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17882-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17882-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="17882-118">O circuito ExpressRoute que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="17882-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="17882-119">Este é o objeto Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="17882-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17882-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="17882-120">-LegacyMode</span></span>
<span data-ttu-id="17882-121">O modo herdamento do Peering</span><span class="sxs-lookup"><span data-stu-id="17882-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="17882-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="17882-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="17882-123">Para um PeeringType do MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que você planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="17882-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="17882-124">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="17882-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="17882-125">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="17882-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="17882-126">Esses prefixos devem ser registrados em um Nome de Registro de Roteamento (RIR/RIR).</span><span class="sxs-lookup"><span data-stu-id="17882-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="17882-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="17882-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="17882-128">Se você estiver anunciando prefixos que não estão registrados no número AS de paração, você poderá especificar o número AS ao qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="17882-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="17882-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="17882-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="17882-130">O Nome do Registro de Roteamento (RIR/RIR) ao qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="17882-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="17882-131">-Name</span><span class="sxs-lookup"><span data-stu-id="17882-131">-Name</span></span>
<span data-ttu-id="17882-132">O nome da relação de paração a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="17882-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="17882-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="17882-133">-PeerAddressType</span></span>
<span data-ttu-id="17882-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="17882-134">PeerAddressType</span></span>

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

### <span data-ttu-id="17882-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="17882-135">-PeerASN</span></span>
<span data-ttu-id="17882-136">O número AS do seu circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17882-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="17882-137">Deve ser uma ASN Pública quando PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="17882-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="17882-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="17882-138">-PeeringType</span></span>
<span data-ttu-id="17882-139">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="17882-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="17882-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="17882-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="17882-141">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="17882-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="17882-142">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="17882-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="17882-143">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="17882-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="17882-144">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="17882-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="17882-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="17882-145">-RouteFilter</span></span>
<span data-ttu-id="17882-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="17882-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="17882-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="17882-147">-RouteFilterId</span></span>
<span data-ttu-id="17882-148">Essa é a ID de recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="17882-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="17882-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="17882-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="17882-150">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="17882-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="17882-151">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="17882-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="17882-152">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="17882-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="17882-153">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="17882-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="17882-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="17882-154">-SharedKey</span></span>
<span data-ttu-id="17882-155">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="17882-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="17882-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="17882-156">-VlanId</span></span>
<span data-ttu-id="17882-157">Esse é o número de Id da VLAN atribuída a esse paring.</span><span class="sxs-lookup"><span data-stu-id="17882-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="17882-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17882-158">CommonParameters</span></span>
<span data-ttu-id="17882-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17882-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17882-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17882-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17882-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17882-161">INPUTS</span></span>

### <span data-ttu-id="17882-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17882-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="17882-163">System.String</span><span class="sxs-lookup"><span data-stu-id="17882-163">System.String</span></span>

### <span data-ttu-id="17882-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="17882-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="17882-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17882-165">System.Boolean</span></span>

## <span data-ttu-id="17882-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17882-166">OUTPUTS</span></span>

### <span data-ttu-id="17882-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17882-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="17882-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="17882-168">NOTES</span></span>

## <span data-ttu-id="17882-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17882-169">RELATED LINKS</span></span>

[<span data-ttu-id="17882-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17882-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="17882-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="17882-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="17882-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="17882-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="17882-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17882-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
