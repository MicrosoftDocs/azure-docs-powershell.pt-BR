---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 87c956769efb41485e43e65ff31d7a9cd7387d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440197"
---
# <span data-ttu-id="ec59c-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec59c-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ec59c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec59c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec59c-103">Salva uma configuração de emparelhamento do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="ec59c-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec59c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec59c-104">SYNTAX</span></span>

### <span data-ttu-id="ec59c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec59c-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec59c-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="ec59c-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec59c-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="ec59c-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec59c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec59c-108">DESCRIPTION</span></span>
<span data-ttu-id="ec59c-109">Os cmdlets **set-AzureRmExpressRouteCircuitPeeringConfig** salvam uma configuração de emparelhamento de rota modificada de volta para o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec59c-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="ec59c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec59c-110">EXAMPLES</span></span>

### <span data-ttu-id="ec59c-111">Exemplo 1: alterar uma configuração de emparelhamento existente</span><span class="sxs-lookup"><span data-stu-id="ec59c-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ec59c-112">OS</span><span class="sxs-lookup"><span data-stu-id="ec59c-112">PARAMETERS</span></span>

### <span data-ttu-id="ec59c-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec59c-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ec59c-114">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ec59c-114">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="ec59c-115">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="ec59c-115">-LegacyMode</span></span>
<span data-ttu-id="ec59c-116">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="ec59c-116">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="ec59c-117">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="ec59c-117">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="ec59c-118">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="ec59c-118">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ec59c-119">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="ec59c-119">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ec59c-120">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="ec59c-120">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ec59c-121">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="ec59c-121">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ec59c-122">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ec59c-122">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ec59c-123">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="ec59c-123">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ec59c-124">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ec59c-124">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ec59c-125">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="ec59c-125">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ec59c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec59c-126">-Name</span></span>
<span data-ttu-id="ec59c-127">O nome da configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ec59c-127">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="ec59c-128">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ec59c-128">-PeerAddressType</span></span>
<span data-ttu-id="ec59c-129">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ec59c-129">PeerAddressType</span></span>

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

### <span data-ttu-id="ec59c-130">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="ec59c-130">-PeerASN</span></span>
<span data-ttu-id="ec59c-131">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec59c-131">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="ec59c-132">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="ec59c-132">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ec59c-133">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ec59c-133">-PeeringType</span></span>
<span data-ttu-id="ec59c-134">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ec59c-134">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ec59c-135">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ec59c-135">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ec59c-136">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ec59c-136">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ec59c-137">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="ec59c-137">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ec59c-138">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="ec59c-138">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ec59c-139">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec59c-139">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ec59c-140">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec59c-140">-RouteFilter</span></span>
<span data-ttu-id="ec59c-141">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="ec59c-141">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ec59c-142">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="ec59c-142">-RouteFilterId</span></span>
<span data-ttu-id="ec59c-143">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="ec59c-143">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="ec59c-144">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ec59c-144">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ec59c-145">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ec59c-145">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ec59c-146">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="ec59c-146">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ec59c-147">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="ec59c-147">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ec59c-148">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec59c-148">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ec59c-149">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ec59c-149">-SharedKey</span></span>
<span data-ttu-id="ec59c-150">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="ec59c-150">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ec59c-151">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="ec59c-151">-VlanId</span></span>
<span data-ttu-id="ec59c-152">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="ec59c-152">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ec59c-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec59c-153">-DefaultProfile</span></span>
<span data-ttu-id="ec59c-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec59c-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec59c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec59c-155">CommonParameters</span></span>
<span data-ttu-id="ec59c-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec59c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec59c-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec59c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec59c-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec59c-158">INPUTS</span></span>

### <span data-ttu-id="ec59c-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec59c-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ec59c-160">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ec59c-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="ec59c-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec59c-161">OUTPUTS</span></span>

### <span data-ttu-id="ec59c-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec59c-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ec59c-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec59c-163">NOTES</span></span>

## <span data-ttu-id="ec59c-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec59c-164">RELATED LINKS</span></span>

[<span data-ttu-id="ec59c-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec59c-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec59c-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec59c-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ec59c-167">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec59c-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec59c-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec59c-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)
