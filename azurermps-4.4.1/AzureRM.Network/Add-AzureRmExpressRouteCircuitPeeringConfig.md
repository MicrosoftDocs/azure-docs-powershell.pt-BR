---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441018"
---
# <span data-ttu-id="1b095-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1b095-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1b095-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b095-102">SYNOPSIS</span></span>
<span data-ttu-id="1b095-103">Adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b095-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b095-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b095-104">SYNTAX</span></span>

### <span data-ttu-id="1b095-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b095-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b095-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="1b095-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b095-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="1b095-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b095-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b095-108">DESCRIPTION</span></span>
<span data-ttu-id="1b095-109">O cmdlet **Add-AzureRmExpressRouteCircuitPeeringConfig** adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b095-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="1b095-110">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="1b095-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1b095-111">Observe que, depois de executar **Add-AzureRmExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzureRmExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="1b095-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="1b095-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b095-112">EXAMPLES</span></span>

### <span data-ttu-id="1b095-113">Exemplo 1: adicionar um par a um circuito do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="1b095-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="1b095-114">OS</span><span class="sxs-lookup"><span data-stu-id="1b095-114">PARAMETERS</span></span>

### <span data-ttu-id="1b095-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1b095-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1b095-116">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="1b095-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="1b095-117">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="1b095-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="1b095-118">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="1b095-118">-LegacyMode</span></span>
<span data-ttu-id="1b095-119">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="1b095-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="1b095-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="1b095-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="1b095-121">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="1b095-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="1b095-122">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="1b095-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="1b095-123">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="1b095-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="1b095-124">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="1b095-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="1b095-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="1b095-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="1b095-126">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="1b095-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="1b095-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="1b095-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="1b095-128">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="1b095-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="1b095-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b095-129">-Name</span></span>
<span data-ttu-id="1b095-130">O nome da relação de emparelhamento a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="1b095-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="1b095-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1b095-131">-PeerAddressType</span></span>
<span data-ttu-id="1b095-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1b095-132">PeerAddressType</span></span>

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

### <span data-ttu-id="1b095-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="1b095-133">-PeerASN</span></span>
<span data-ttu-id="1b095-134">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1b095-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="1b095-135">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="1b095-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="1b095-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1b095-136">-PeeringType</span></span>
<span data-ttu-id="1b095-137">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1b095-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1b095-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1b095-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="1b095-139">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="1b095-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="1b095-140">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="1b095-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1b095-141">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="1b095-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1b095-142">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b095-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1b095-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b095-143">-RouteFilter</span></span>
<span data-ttu-id="1b095-144">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="1b095-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1b095-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="1b095-145">-RouteFilterId</span></span>
<span data-ttu-id="1b095-146">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="1b095-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1b095-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1b095-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="1b095-148">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="1b095-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="1b095-149">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="1b095-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1b095-150">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="1b095-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1b095-151">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b095-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1b095-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1b095-152">-SharedKey</span></span>
<span data-ttu-id="1b095-153">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="1b095-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="1b095-154">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="1b095-154">-VlanId</span></span>
<span data-ttu-id="1b095-155">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="1b095-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="1b095-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b095-156">-DefaultProfile</span></span>
<span data-ttu-id="1b095-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b095-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b095-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b095-158">CommonParameters</span></span>
<span data-ttu-id="1b095-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b095-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b095-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b095-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b095-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b095-161">INPUTS</span></span>

### <span data-ttu-id="1b095-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1b095-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="1b095-163">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1b095-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="1b095-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b095-164">OUTPUTS</span></span>

### <span data-ttu-id="1b095-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1b095-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1b095-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b095-166">NOTES</span></span>

## <span data-ttu-id="1b095-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b095-167">RELATED LINKS</span></span>

[<span data-ttu-id="1b095-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1b095-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1b095-169">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1b095-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1b095-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1b095-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1b095-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1b095-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
