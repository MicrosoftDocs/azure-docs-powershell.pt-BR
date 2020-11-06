---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 73b62d6615c1c443aaad77b38b9ae451a15b181c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440367"
---
# <span data-ttu-id="7dd64-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7dd64-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="7dd64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dd64-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd64-103">Adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7dd64-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dd64-104">SYNTAX</span></span>

### <span data-ttu-id="7dd64-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7dd64-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd64-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="7dd64-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd64-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="7dd64-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd64-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dd64-108">DESCRIPTION</span></span>
<span data-ttu-id="7dd64-109">O cmdlet **Add-AzureRmExpressRouteCircuitPeeringConfig** adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7dd64-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="7dd64-110">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="7dd64-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="7dd64-111">Observe que, depois de executar **Add-AzureRmExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzureRmExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="7dd64-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="7dd64-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dd64-112">EXAMPLES</span></span>

### <span data-ttu-id="7dd64-113">Exemplo 1: adicionar um par a um circuito do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="7dd64-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="7dd64-114">OS</span><span class="sxs-lookup"><span data-stu-id="7dd64-114">PARAMETERS</span></span>

### <span data-ttu-id="7dd64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd64-115">-DefaultProfile</span></span>
<span data-ttu-id="7dd64-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd64-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd64-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dd64-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7dd64-118">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="7dd64-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="7dd64-119">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="7dd64-119">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="7dd64-120">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="7dd64-120">-LegacyMode</span></span>
<span data-ttu-id="7dd64-121">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="7dd64-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="7dd64-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="7dd64-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="7dd64-123">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="7dd64-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="7dd64-124">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="7dd64-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="7dd64-125">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="7dd64-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="7dd64-126">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="7dd64-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="7dd64-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="7dd64-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="7dd64-128">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="7dd64-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="7dd64-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="7dd64-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="7dd64-130">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="7dd64-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="7dd64-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dd64-131">-Name</span></span>
<span data-ttu-id="7dd64-132">O nome da relação de emparelhamento a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7dd64-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="7dd64-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7dd64-133">-PeerAddressType</span></span>
<span data-ttu-id="7dd64-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7dd64-134">PeerAddressType</span></span>

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

### <span data-ttu-id="7dd64-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="7dd64-135">-PeerASN</span></span>
<span data-ttu-id="7dd64-136">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7dd64-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="7dd64-137">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="7dd64-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="7dd64-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7dd64-138">-PeeringType</span></span>
<span data-ttu-id="7dd64-139">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7dd64-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7dd64-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7dd64-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="7dd64-141">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7dd64-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="7dd64-142">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="7dd64-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7dd64-143">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="7dd64-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7dd64-144">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd64-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7dd64-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dd64-145">-RouteFilter</span></span>
<span data-ttu-id="7dd64-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="7dd64-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7dd64-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="7dd64-147">-RouteFilterId</span></span>
<span data-ttu-id="7dd64-148">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="7dd64-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="7dd64-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7dd64-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="7dd64-150">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7dd64-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="7dd64-151">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="7dd64-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7dd64-152">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="7dd64-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7dd64-153">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd64-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7dd64-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7dd64-154">-SharedKey</span></span>
<span data-ttu-id="7dd64-155">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7dd64-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="7dd64-156">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="7dd64-156">-VlanId</span></span>
<span data-ttu-id="7dd64-157">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="7dd64-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="7dd64-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd64-158">CommonParameters</span></span>
<span data-ttu-id="7dd64-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd64-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd64-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd64-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd64-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dd64-161">INPUTS</span></span>

### <span data-ttu-id="7dd64-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dd64-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="7dd64-163">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7dd64-163">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="7dd64-164">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd64-164">System.String</span></span>

### <span data-ttu-id="7dd64-165">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dd64-165">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="7dd64-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7dd64-166">System.Boolean</span></span>

## <span data-ttu-id="7dd64-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dd64-167">OUTPUTS</span></span>

### <span data-ttu-id="7dd64-168">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dd64-168">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7dd64-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dd64-169">NOTES</span></span>

## <span data-ttu-id="7dd64-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dd64-170">RELATED LINKS</span></span>

[<span data-ttu-id="7dd64-171">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dd64-171">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7dd64-172">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7dd64-172">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7dd64-173">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7dd64-173">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7dd64-174">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dd64-174">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
