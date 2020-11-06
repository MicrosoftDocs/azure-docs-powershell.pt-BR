---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ecbd0d101db979d5982891bbfbd4ad1e3083ee8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600023"
---
# <span data-ttu-id="ab6db-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ab6db-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ab6db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab6db-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6db-103">Salva uma configuração de emparelhamento do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="ab6db-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="ab6db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab6db-104">SYNTAX</span></span>

### <span data-ttu-id="ab6db-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab6db-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6db-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="ab6db-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6db-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="ab6db-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab6db-108">DESCRIPTION</span></span>
<span data-ttu-id="ab6db-109">Os cmdlets **set-AzExpressRouteCircuitPeeringConfig** salvam uma configuração de emparelhamento de rota modificada de volta para o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6db-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="ab6db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab6db-110">EXAMPLES</span></span>

### <span data-ttu-id="ab6db-111">Exemplo 1: alterar uma configuração de emparelhamento existente</span><span class="sxs-lookup"><span data-stu-id="ab6db-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="ab6db-112">OS</span><span class="sxs-lookup"><span data-stu-id="ab6db-112">PARAMETERS</span></span>

### <span data-ttu-id="ab6db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6db-113">-DefaultProfile</span></span>
<span data-ttu-id="ab6db-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6db-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab6db-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ab6db-116">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ab6db-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="ab6db-117">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="ab6db-117">-LegacyMode</span></span>
<span data-ttu-id="ab6db-118">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="ab6db-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="ab6db-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="ab6db-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="ab6db-120">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="ab6db-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ab6db-121">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="ab6db-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ab6db-122">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="ab6db-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ab6db-123">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="ab6db-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ab6db-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ab6db-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ab6db-125">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="ab6db-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ab6db-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ab6db-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ab6db-127">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="ab6db-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ab6db-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab6db-128">-Name</span></span>
<span data-ttu-id="ab6db-129">O nome da configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ab6db-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="ab6db-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ab6db-130">-PeerAddressType</span></span>
<span data-ttu-id="ab6db-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ab6db-131">PeerAddressType</span></span>

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

### <span data-ttu-id="ab6db-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ab6db-132">-PeerASN</span></span>
<span data-ttu-id="ab6db-133">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab6db-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="ab6db-134">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="ab6db-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ab6db-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ab6db-135">-PeeringType</span></span>
<span data-ttu-id="ab6db-136">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ab6db-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ab6db-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab6db-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ab6db-138">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ab6db-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ab6db-139">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="ab6db-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ab6db-140">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="ab6db-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ab6db-141">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6db-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ab6db-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ab6db-142">-RouteFilter</span></span>
<span data-ttu-id="ab6db-143">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="ab6db-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ab6db-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="ab6db-144">-RouteFilterId</span></span>
<span data-ttu-id="ab6db-145">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="ab6db-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ab6db-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab6db-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ab6db-147">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ab6db-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ab6db-148">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="ab6db-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ab6db-149">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="ab6db-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ab6db-150">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6db-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ab6db-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ab6db-151">-SharedKey</span></span>
<span data-ttu-id="ab6db-152">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ab6db-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ab6db-153">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="ab6db-153">-VlanId</span></span>
<span data-ttu-id="ab6db-154">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="ab6db-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ab6db-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6db-155">CommonParameters</span></span>
<span data-ttu-id="ab6db-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6db-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6db-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6db-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6db-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab6db-158">INPUTS</span></span>

### <span data-ttu-id="ab6db-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab6db-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="ab6db-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ab6db-160">System.String</span></span>

### <span data-ttu-id="ab6db-161">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ab6db-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="ab6db-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab6db-162">System.Boolean</span></span>

## <span data-ttu-id="ab6db-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab6db-163">OUTPUTS</span></span>

### <span data-ttu-id="ab6db-164">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab6db-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ab6db-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab6db-165">NOTES</span></span>

## <span data-ttu-id="ab6db-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab6db-166">RELATED LINKS</span></span>

[<span data-ttu-id="ab6db-167">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ab6db-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ab6db-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab6db-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ab6db-169">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ab6db-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ab6db-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ab6db-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
