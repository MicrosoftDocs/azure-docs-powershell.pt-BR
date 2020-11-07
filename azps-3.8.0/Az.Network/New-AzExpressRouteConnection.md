---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 135b865f5b083ca96af6f518a4dec7d48584f72a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942517"
---
# <span data-ttu-id="86e89-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="86e89-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="86e89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86e89-102">SYNOPSIS</span></span>
<span data-ttu-id="86e89-103">Cria uma conexão do ExpressRoute que conecta um gateway do ExpressRoute a um circuito do ExpressRoute no local.</span><span class="sxs-lookup"><span data-stu-id="86e89-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="86e89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86e89-104">SYNTAX</span></span>

### <span data-ttu-id="86e89-105">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="86e89-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e89-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="86e89-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e89-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="86e89-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e89-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86e89-108">DESCRIPTION</span></span>
<span data-ttu-id="86e89-109">Cria uma conexão do ExpressRoute entre um emparelhamento BGP do circuito no local ExpressRoute para o gateway do ExpressRoute dentro de um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="86e89-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="86e89-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86e89-110">EXAMPLES</span></span>

### <span data-ttu-id="86e89-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86e89-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="86e89-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual, o gateway de rota expressa e um circuito do ExpressRoute com emparelhamento privado no centro-oeste do grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="86e89-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="86e89-113">Após a criação do gateway, ele é conectado à troca de circuito do ExpressRoute usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="86e89-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="86e89-114">OS</span><span class="sxs-lookup"><span data-stu-id="86e89-114">PARAMETERS</span></span>

### <span data-ttu-id="86e89-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86e89-115">-AsJob</span></span>
<span data-ttu-id="86e89-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="86e89-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="86e89-117">-AuthorizationKey</span></span>
<span data-ttu-id="86e89-118">Uma chave obtida do proprietário do circuito do ExpressRoute para poder criar uma conexão com um gateway em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="86e89-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="86e89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e89-119">-DefaultProfile</span></span>
<span data-ttu-id="86e89-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86e89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="86e89-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="86e89-122">Habilitar a segurança da Internet para esta conexão de gateway ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="86e89-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="86e89-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="86e89-124">A ID do recurso do emparelhamento de circuito de rota expressa para a qual essa conexão de gateway de rota expressa deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="86e89-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="86e89-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="86e89-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="86e89-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86e89-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="86e89-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="86e89-128">O ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="86e89-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="86e89-129">-Name</span></span>
<span data-ttu-id="86e89-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="86e89-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86e89-131">-ParentResourceId</span></span>
<span data-ttu-id="86e89-132">A ID do recurso do ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="86e89-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e89-133">-ResourceGroupName</span></span>
<span data-ttu-id="86e89-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86e89-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-135">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="86e89-135">-RoutingWeight</span></span>
<span data-ttu-id="86e89-136">O peso do roteamento de pacotes que precisa ser atribuído a essa conexão.</span><span class="sxs-lookup"><span data-stu-id="86e89-136">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86e89-137">-Confirm</span></span>
<span data-ttu-id="86e89-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86e89-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e89-139">-WhatIf</span></span>
<span data-ttu-id="86e89-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86e89-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e89-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86e89-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e89-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e89-142">CommonParameters</span></span>
<span data-ttu-id="86e89-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e89-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e89-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86e89-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e89-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86e89-145">INPUTS</span></span>

### <span data-ttu-id="86e89-146">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="86e89-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="86e89-147">System. String</span><span class="sxs-lookup"><span data-stu-id="86e89-147">System.String</span></span>

## <span data-ttu-id="86e89-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86e89-148">OUTPUTS</span></span>

### <span data-ttu-id="86e89-149">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="86e89-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="86e89-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86e89-150">NOTES</span></span>

## <span data-ttu-id="86e89-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86e89-151">RELATED LINKS</span></span>
