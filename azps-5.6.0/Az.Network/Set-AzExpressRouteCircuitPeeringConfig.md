---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 42a2ec1c3fb19647cc956c6b7321f52e6ad6e63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885391"
---
# <span data-ttu-id="e16b9-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e16b9-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e16b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e16b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e16b9-103">Salva uma configuração de paração ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="e16b9-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="e16b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e16b9-104">SYNTAX</span></span>

### <span data-ttu-id="e16b9-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e16b9-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16b9-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="e16b9-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16b9-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="e16b9-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e16b9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e16b9-108">DESCRIPTION</span></span>
<span data-ttu-id="e16b9-109">Os cmdlets **Set-AzExpressRouteCircuitPeeringConfig** salvam uma configuração de paração ExpressRoute modificada de volta para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e16b9-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="e16b9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e16b9-110">EXAMPLES</span></span>

### <span data-ttu-id="e16b9-111">Exemplo 1: Alterar uma configuração de peering existente</span><span class="sxs-lookup"><span data-stu-id="e16b9-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="e16b9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e16b9-112">Example 2</span></span>

<span data-ttu-id="e16b9-113">Salva uma configuração de paração ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="e16b9-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="e16b9-114">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e16b9-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="e16b9-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e16b9-115">PARAMETERS</span></span>

### <span data-ttu-id="e16b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16b9-116">-DefaultProfile</span></span>
<span data-ttu-id="e16b9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e16b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e16b9-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e16b9-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e16b9-119">O objeto de circuito ExpressRoute que contém a configuração de paração a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="e16b9-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="e16b9-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="e16b9-120">-LegacyMode</span></span>
<span data-ttu-id="e16b9-121">O modo herdamento do Peering</span><span class="sxs-lookup"><span data-stu-id="e16b9-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="e16b9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="e16b9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="e16b9-123">Para um PeeringType do MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que você planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="e16b9-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e16b9-124">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="e16b9-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e16b9-125">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="e16b9-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e16b9-126">Esses prefixos devem ser registrados em um Nome de Registro de Roteamento (RIR/RIR).</span><span class="sxs-lookup"><span data-stu-id="e16b9-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="e16b9-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e16b9-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e16b9-128">Se você estiver anunciando prefixos que não estão registrados no número AS de paração, você poderá especificar o número AS ao qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="e16b9-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="e16b9-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e16b9-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e16b9-130">O Nome do Registro de Roteamento (RIR/RIR) ao qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="e16b9-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="e16b9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e16b9-131">-Name</span></span>
<span data-ttu-id="e16b9-132">O nome da configuração de paração a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="e16b9-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="e16b9-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e16b9-133">-PeerAddressType</span></span>
<span data-ttu-id="e16b9-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e16b9-134">PeerAddressType</span></span>

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

### <span data-ttu-id="e16b9-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="e16b9-135">-PeerASN</span></span>
<span data-ttu-id="e16b9-136">O número AS do seu circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e16b9-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="e16b9-137">Deve ser uma ASN Pública quando PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="e16b9-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="e16b9-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e16b9-138">-PeeringType</span></span>
<span data-ttu-id="e16b9-139">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e16b9-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e16b9-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e16b9-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e16b9-141">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="e16b9-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e16b9-142">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="e16b9-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e16b9-143">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="e16b9-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e16b9-144">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="e16b9-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e16b9-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e16b9-145">-RouteFilter</span></span>
<span data-ttu-id="e16b9-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="e16b9-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e16b9-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="e16b9-147">-RouteFilterId</span></span>
<span data-ttu-id="e16b9-148">Essa é a ID de recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="e16b9-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e16b9-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e16b9-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e16b9-150">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de paridade.</span><span class="sxs-lookup"><span data-stu-id="e16b9-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e16b9-151">Deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="e16b9-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e16b9-152">O primeiro endereço numerado ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="e16b9-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e16b9-153">O Azure configurará o próximo endereço numerado para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="e16b9-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e16b9-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e16b9-154">-SharedKey</span></span>
<span data-ttu-id="e16b9-155">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="e16b9-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="e16b9-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="e16b9-156">-VlanId</span></span>
<span data-ttu-id="e16b9-157">Esse é o número de Id da VLAN atribuída a esse paring.</span><span class="sxs-lookup"><span data-stu-id="e16b9-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="e16b9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16b9-158">CommonParameters</span></span>
<span data-ttu-id="e16b9-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e16b9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16b9-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e16b9-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16b9-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e16b9-161">INPUTS</span></span>

### <span data-ttu-id="e16b9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e16b9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="e16b9-163">System.String</span><span class="sxs-lookup"><span data-stu-id="e16b9-163">System.String</span></span>

### <span data-ttu-id="e16b9-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e16b9-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="e16b9-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e16b9-165">System.Boolean</span></span>

## <span data-ttu-id="e16b9-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e16b9-166">OUTPUTS</span></span>

### <span data-ttu-id="e16b9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e16b9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e16b9-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="e16b9-168">NOTES</span></span>

## <span data-ttu-id="e16b9-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e16b9-169">RELATED LINKS</span></span>

[<span data-ttu-id="e16b9-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e16b9-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e16b9-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e16b9-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e16b9-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e16b9-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e16b9-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e16b9-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
