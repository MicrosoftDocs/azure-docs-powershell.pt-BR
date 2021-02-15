---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112768"
---
# <span data-ttu-id="53efd-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="53efd-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="53efd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53efd-102">SYNOPSIS</span></span>
<span data-ttu-id="53efd-103">Salva uma configuração de peering do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="53efd-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="53efd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53efd-104">SYNTAX</span></span>

### <span data-ttu-id="53efd-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="53efd-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53efd-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="53efd-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53efd-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="53efd-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53efd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="53efd-108">DESCRIPTION</span></span>
<span data-ttu-id="53efd-109">Os cmdlets **Set-AzExpressRoute CircuitPeeringConfig** salvam uma configuração de peering do ExpressRoute modificada de volta ao Azure.</span><span class="sxs-lookup"><span data-stu-id="53efd-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="53efd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53efd-110">EXAMPLES</span></span>

### <span data-ttu-id="53efd-111">Exemplo 1: Alterar uma configuração de paridade existente</span><span class="sxs-lookup"><span data-stu-id="53efd-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="53efd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53efd-112">Example 2</span></span>

<span data-ttu-id="53efd-113">Salva uma configuração de peering do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="53efd-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="53efd-114">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="53efd-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="53efd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53efd-115">PARAMETERS</span></span>

### <span data-ttu-id="53efd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53efd-116">-DefaultProfile</span></span>
<span data-ttu-id="53efd-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="53efd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53efd-118">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="53efd-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="53efd-119">O objeto de circuito do ExpressRoute que contém a configuração de peering a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="53efd-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="53efd-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="53efd-120">-LegacyMode</span></span>
<span data-ttu-id="53efd-121">O modo herdário do Peering</span><span class="sxs-lookup"><span data-stu-id="53efd-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="53efd-122">-MicrosoftConfigAdvertedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="53efd-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="53efd-123">Para um PeeringType da MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que planeja anunciar durante a sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="53efd-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="53efd-124">Somente prefixos de endereço IP públicos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="53efd-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="53efd-125">Você pode enviar uma lista separada por vírgulas se planeja enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="53efd-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="53efd-126">Esses prefixos devem ser registrados para você em um Nome de Registro de Roteamento (SEMPRE/IRR).</span><span class="sxs-lookup"><span data-stu-id="53efd-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="53efd-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="53efd-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="53efd-128">Se você estiver anunciando prefixos que não estão registrados no número AS de par, poderá especificar o número AS para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="53efd-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="53efd-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="53efd-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="53efd-130">O Nome do Registro de Roteamento (NÚM/IRR) para o qual o número AS e os prefixos estão registrados.</span><span class="sxs-lookup"><span data-stu-id="53efd-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="53efd-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="53efd-131">-Name</span></span>
<span data-ttu-id="53efd-132">O nome da configuração de peering a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="53efd-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="53efd-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="53efd-133">-PeerAddressType</span></span>
<span data-ttu-id="53efd-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="53efd-134">PeerAddressType</span></span>

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

### <span data-ttu-id="53efd-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="53efd-135">-PeerASN</span></span>
<span data-ttu-id="53efd-136">O número AS do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="53efd-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="53efd-137">Esse deve ser um ASN Público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="53efd-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="53efd-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="53efd-138">-PeeringType</span></span>
<span data-ttu-id="53efd-139">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="53efd-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="53efd-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="53efd-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="53efd-141">Este é o intervalo de Endereços IP para o caminho de roteamento principal dessa relação de peering.</span><span class="sxs-lookup"><span data-stu-id="53efd-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="53efd-142">Essa deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="53efd-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="53efd-143">O primeiro endereço ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="53efd-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="53efd-144">O Azure configurará o próximo endereço de número even para a interface de roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="53efd-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="53efd-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="53efd-145">-RouteFilter</span></span>
<span data-ttu-id="53efd-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="53efd-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="53efd-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="53efd-147">-RouteFilterId</span></span>
<span data-ttu-id="53efd-148">Esta é a ID de recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="53efd-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="53efd-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="53efd-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="53efd-150">Este é o intervalo de Endereços IP para o caminho de roteamento secundário dessa relação de peering.</span><span class="sxs-lookup"><span data-stu-id="53efd-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="53efd-151">Essa deve ser uma sub-rede CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="53efd-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="53efd-152">O primeiro endereço ímpar nesta sub-rede deve ser atribuído à interface do roteador.</span><span class="sxs-lookup"><span data-stu-id="53efd-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="53efd-153">O Azure configurará o próximo endereço de número even para a interface de roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="53efd-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="53efd-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="53efd-154">-SharedKey</span></span>
<span data-ttu-id="53efd-155">Este é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="53efd-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="53efd-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="53efd-156">-VlanId</span></span>
<span data-ttu-id="53efd-157">Este é o número de ID da VLAN atribuída para esse peering.</span><span class="sxs-lookup"><span data-stu-id="53efd-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="53efd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53efd-158">CommonParameters</span></span>
<span data-ttu-id="53efd-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53efd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53efd-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53efd-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53efd-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="53efd-161">INPUTS</span></span>

### <span data-ttu-id="53efd-162">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="53efd-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="53efd-163">System.String</span><span class="sxs-lookup"><span data-stu-id="53efd-163">System.String</span></span>

### <span data-ttu-id="53efd-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="53efd-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="53efd-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53efd-165">System.Boolean</span></span>

## <span data-ttu-id="53efd-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="53efd-166">OUTPUTS</span></span>

### <span data-ttu-id="53efd-167">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="53efd-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="53efd-168">Notas</span><span class="sxs-lookup"><span data-stu-id="53efd-168">NOTES</span></span>

## <span data-ttu-id="53efd-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53efd-169">RELATED LINKS</span></span>

[<span data-ttu-id="53efd-170">Add-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="53efd-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="53efd-171">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="53efd-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="53efd-172">New-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="53efd-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="53efd-173">Remove-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="53efd-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
