---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117248"
---
# <span data-ttu-id="0366a-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0366a-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0366a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0366a-102">SYNOPSIS</span></span>
<span data-ttu-id="0366a-103">Salva uma configuração de emparelhamento do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="0366a-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="0366a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0366a-104">SYNTAX</span></span>

### <span data-ttu-id="0366a-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="0366a-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0366a-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="0366a-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0366a-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="0366a-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0366a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0366a-108">DESCRIPTION</span></span>
<span data-ttu-id="0366a-109">Os cmdlets **set-AzExpressRouteCircuitPeeringConfig** salvam uma configuração de emparelhamento de rota modificada de volta para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0366a-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="0366a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0366a-110">EXAMPLES</span></span>

### <span data-ttu-id="0366a-111">Exemplo 1: alterar uma configuração de emparelhamento existente</span><span class="sxs-lookup"><span data-stu-id="0366a-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="0366a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0366a-112">Example 2</span></span>

<span data-ttu-id="0366a-113">Salva uma configuração de emparelhamento do ExpressRoute modificada.</span><span class="sxs-lookup"><span data-stu-id="0366a-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="0366a-114">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="0366a-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="0366a-115">OS</span><span class="sxs-lookup"><span data-stu-id="0366a-115">PARAMETERS</span></span>

### <span data-ttu-id="0366a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0366a-116">-DefaultProfile</span></span>
<span data-ttu-id="0366a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0366a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0366a-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0366a-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0366a-119">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0366a-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="0366a-120">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="0366a-120">-LegacyMode</span></span>
<span data-ttu-id="0366a-121">O modo herdado do emparelhamento</span><span class="sxs-lookup"><span data-stu-id="0366a-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="0366a-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="0366a-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="0366a-123">Para obter um PeeringType de MicrosoftPeering, você deve fornecer uma lista de todos os prefixos que pretende anunciar pela sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="0366a-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="0366a-124">Somente prefixos de endereço IP público são aceitos.</span><span class="sxs-lookup"><span data-stu-id="0366a-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="0366a-125">Você pode enviar uma lista separada por vírgulas, caso pretenda enviar um conjunto de prefixos.</span><span class="sxs-lookup"><span data-stu-id="0366a-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="0366a-126">Esses prefixos devem ser registrados para você em um nome de registro de roteamento (RIR/TIR).</span><span class="sxs-lookup"><span data-stu-id="0366a-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="0366a-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="0366a-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="0366a-128">Se você for anunciar prefixos que não são registrados para o número de emparelhamento como número, você pode especificar o número as para o qual eles estão registrados.</span><span class="sxs-lookup"><span data-stu-id="0366a-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="0366a-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="0366a-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="0366a-130">O nome do registro de roteamento (RIR/TIR) para o qual o número como e os prefixos são registrados.</span><span class="sxs-lookup"><span data-stu-id="0366a-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="0366a-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0366a-131">-Name</span></span>
<span data-ttu-id="0366a-132">O nome da configuração de emparelhamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="0366a-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="0366a-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0366a-133">-PeerAddressType</span></span>
<span data-ttu-id="0366a-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0366a-134">PeerAddressType</span></span>

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

### <span data-ttu-id="0366a-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="0366a-135">-PeerASN</span></span>
<span data-ttu-id="0366a-136">O número as do seu circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0366a-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="0366a-137">Isso deve ser um ASN público quando o PeeringType for AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="0366a-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="0366a-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0366a-138">-PeeringType</span></span>
<span data-ttu-id="0366a-139">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0366a-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0366a-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0366a-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="0366a-141">Esse é o intervalo de endereços IP para o caminho de roteamento principal dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="0366a-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="0366a-142">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="0366a-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0366a-143">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="0366a-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0366a-144">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="0366a-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="0366a-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0366a-145">-RouteFilter</span></span>
<span data-ttu-id="0366a-146">Este é um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="0366a-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="0366a-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="0366a-147">-RouteFilterId</span></span>
<span data-ttu-id="0366a-148">Esta é a ID do recurso de um objeto RouteFilter existente.</span><span class="sxs-lookup"><span data-stu-id="0366a-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="0366a-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0366a-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="0366a-150">Esse é o intervalo de endereços IP para o caminho de roteamento secundário dessa relação de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="0366a-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="0366a-151">Deve ser uma sub-rede CIDR de/30.</span><span class="sxs-lookup"><span data-stu-id="0366a-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="0366a-152">O primeiro endereço ímpar na sub-rede deve ser atribuído à interface do seu roteador.</span><span class="sxs-lookup"><span data-stu-id="0366a-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="0366a-153">O Azure irá configurar o próximo endereço par para a interface do roteador do Azure.</span><span class="sxs-lookup"><span data-stu-id="0366a-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="0366a-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="0366a-154">-SharedKey</span></span>
<span data-ttu-id="0366a-155">Esse é um hash MD5 opcional usado como uma chave pré-compartilhada para a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="0366a-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="0366a-156">-Vlanid</span><span class="sxs-lookup"><span data-stu-id="0366a-156">-VlanId</span></span>
<span data-ttu-id="0366a-157">Este é o número de identificação da VLAN atribuída a essa correspondência.</span><span class="sxs-lookup"><span data-stu-id="0366a-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="0366a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0366a-158">CommonParameters</span></span>
<span data-ttu-id="0366a-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0366a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0366a-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0366a-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0366a-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0366a-161">INPUTS</span></span>

### <span data-ttu-id="0366a-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0366a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="0366a-163">System. String</span><span class="sxs-lookup"><span data-stu-id="0366a-163">System.String</span></span>

### <span data-ttu-id="0366a-164">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0366a-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="0366a-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0366a-165">System.Boolean</span></span>

## <span data-ttu-id="0366a-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0366a-166">OUTPUTS</span></span>

### <span data-ttu-id="0366a-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0366a-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0366a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0366a-168">NOTES</span></span>

## <span data-ttu-id="0366a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0366a-169">RELATED LINKS</span></span>

[<span data-ttu-id="0366a-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0366a-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0366a-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0366a-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0366a-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0366a-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0366a-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0366a-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
