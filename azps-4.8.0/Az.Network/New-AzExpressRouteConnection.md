---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114368"
---
# <span data-ttu-id="6d3c9-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6d3c9-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="6d3c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3c9-103">Cria uma conexão do ExpressRoute que conecta um gateway do ExpressRoute a um circuito do ExpressRoute no local.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="6d3c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d3c9-104">SYNTAX</span></span>

### <span data-ttu-id="6d3c9-105">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d3c9-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3c9-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6d3c9-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3c9-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6d3c9-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d3c9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d3c9-108">DESCRIPTION</span></span>
<span data-ttu-id="6d3c9-109">Cria uma conexão do ExpressRoute entre um emparelhamento BGP do circuito no local ExpressRoute para o gateway do ExpressRoute dentro de um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="6d3c9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d3c9-110">EXAMPLES</span></span>

### <span data-ttu-id="6d3c9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d3c9-111">Example 1</span></span>

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
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="6d3c9-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual, o gateway de rota expressa e um circuito do ExpressRoute com emparelhamento privado no centro-oeste do grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6d3c9-113">Após a criação do gateway, ele é conectado à troca de circuito do ExpressRoute usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="6d3c9-114">OS</span><span class="sxs-lookup"><span data-stu-id="6d3c9-114">PARAMETERS</span></span>

### <span data-ttu-id="6d3c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d3c9-115">-AsJob</span></span>
<span data-ttu-id="6d3c9-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d3c9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d3c9-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6d3c9-117">-AuthorizationKey</span></span>
<span data-ttu-id="6d3c9-118">Uma chave obtida do proprietário do circuito do ExpressRoute para poder criar uma conexão com um gateway em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="6d3c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3c9-119">-DefaultProfile</span></span>
<span data-ttu-id="6d3c9-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d3c9-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6d3c9-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="6d3c9-122">Habilitar a segurança da Internet para esta conexão de gateway ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6d3c9-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="6d3c9-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="6d3c9-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="6d3c9-124">A ID do recurso do emparelhamento de circuito de rota expressa para a qual essa conexão de gateway de rota expressa deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="6d3c9-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="6d3c9-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="6d3c9-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-126">The resource group name.</span></span>

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

### <span data-ttu-id="6d3c9-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6d3c9-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="6d3c9-128">O ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="6d3c9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d3c9-129">-Name</span></span>
<span data-ttu-id="6d3c9-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-130">The resource name.</span></span>

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

### <span data-ttu-id="6d3c9-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6d3c9-131">-ParentResourceId</span></span>
<span data-ttu-id="6d3c9-132">A ID do recurso do ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="6d3c9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3c9-133">-ResourceGroupName</span></span>
<span data-ttu-id="6d3c9-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-134">The resource group name.</span></span>

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

### <span data-ttu-id="6d3c9-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d3c9-135">-RoutingConfiguration</span></span>
<span data-ttu-id="6d3c9-136">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="6d3c9-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3c9-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6d3c9-137">-RoutingWeight</span></span>
<span data-ttu-id="6d3c9-138">O peso do roteamento de pacotes que precisa ser atribuído a essa conexão.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="6d3c9-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d3c9-139">-Confirm</span></span>
<span data-ttu-id="6d3c9-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d3c9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3c9-141">-WhatIf</span></span>
<span data-ttu-id="6d3c9-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d3c9-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d3c9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3c9-144">CommonParameters</span></span>
<span data-ttu-id="6d3c9-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3c9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3c9-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d3c9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3c9-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d3c9-147">INPUTS</span></span>

### <span data-ttu-id="6d3c9-148">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6d3c9-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="6d3c9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6d3c9-149">System.String</span></span>

## <span data-ttu-id="6d3c9-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d3c9-150">OUTPUTS</span></span>

### <span data-ttu-id="6d3c9-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6d3c9-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="6d3c9-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d3c9-152">NOTES</span></span>

## <span data-ttu-id="6d3c9-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d3c9-153">RELATED LINKS</span></span>

[<span data-ttu-id="6d3c9-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d3c9-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
