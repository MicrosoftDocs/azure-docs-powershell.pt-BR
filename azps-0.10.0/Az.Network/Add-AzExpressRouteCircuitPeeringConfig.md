---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 95c361199e813d5a79bd8f49858ad8d924bd02f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775644"
---
# <span data-ttu-id="f8916-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8916-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f8916-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8916-102">SYNOPSIS</span></span>
<span data-ttu-id="f8916-103">Adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8916-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f8916-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8916-104">SYNTAX</span></span>

### <span data-ttu-id="f8916-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8916-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8916-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="f8916-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8916-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="f8916-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8916-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8916-108">DESCRIPTION</span></span>
<span data-ttu-id="f8916-109">O cmdlet **Add-AzExpressRouteCircuitPeeringConfig** adiciona uma configuração de emparelhamento a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8916-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="f8916-110">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="f8916-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="f8916-111">Observe que, depois de executar **Add-AzExpressRouteCircuitPeeringConfig** , você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a configuração.</span><span class="sxs-lookup"><span data-stu-id="f8916-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="f8916-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8916-112">EXAMPLES</span></span>

### <span data-ttu-id="f8916-113">Exemplo 1: adicionar um par a um circuito do ExpressRoute existente</span><span class="sxs-lookup"><span data-stu-id="f8916-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="f8916-114">OS</span><span class="sxs-lookup"><span data-stu-id="f8916-114">PARAMETERS</span></span>

### <span data-ttu-id="f8916-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8916-115">-DefaultProfile</span></span>
<span data-ttu-id="f8916-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8916-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8916-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f8916-118">O circuito do ExpressRoute sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="f8916-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="f8916-119">Esse é o objeto do Azure retornado pelo cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="f8916-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-120">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="f8916-120">-LegacyMode</span></span>
<span data-ttu-id="f8916-121">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="f8916-121">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="f8916-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="f8916-123">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="f8916-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="f8916-124">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="f8916-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="f8916-125">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="f8916-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="f8916-126">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="f8916-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="f8916-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="f8916-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="f8916-128">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="f8916-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="f8916-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="f8916-130">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="f8916-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8916-131">-Name</span></span>
<span data-ttu-id="f8916-132">O nome da relação de emparelhamento a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="f8916-132">The name of the peering relationship to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f8916-133">-PeerAddressType</span></span>
<span data-ttu-id="f8916-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f8916-134">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="f8916-135">-PeerASN</span></span>
<span data-ttu-id="f8916-136">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8916-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="f8916-137">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="f8916-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f8916-138">-PeeringType</span></span>
<span data-ttu-id="f8916-139">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f8916-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8916-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="f8916-141">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f8916-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="f8916-142">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="f8916-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f8916-143">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="f8916-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f8916-144">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8916-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f8916-145">-RouteFilter</span></span>
<span data-ttu-id="f8916-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="f8916-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="f8916-147">-RouteFilterId</span></span>
<span data-ttu-id="f8916-148">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="f8916-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8916-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="f8916-150">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f8916-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="f8916-151">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="f8916-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="f8916-152">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="f8916-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="f8916-153">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8916-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f8916-154">-SharedKey</span></span>
<span data-ttu-id="f8916-155">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f8916-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-156">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="f8916-156">-VlanId</span></span>
<span data-ttu-id="f8916-157">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="f8916-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8916-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8916-158">CommonParameters</span></span>
<span data-ttu-id="f8916-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8916-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8916-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8916-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8916-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8916-161">INPUTS</span></span>

### <span data-ttu-id="f8916-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8916-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f8916-163">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f8916-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="f8916-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8916-164">OUTPUTS</span></span>

### <span data-ttu-id="f8916-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8916-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f8916-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8916-166">NOTES</span></span>

## <span data-ttu-id="f8916-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8916-167">RELATED LINKS</span></span>

[<span data-ttu-id="f8916-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8916-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f8916-169">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8916-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8916-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8916-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8916-171">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8916-171">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)