---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: ad31bd55c86a785ce45a7f2ca43a20f5a1a97c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886892"
---
# <span data-ttu-id="7b4c7-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7b4c7-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="7b4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4c7-103">Atualiza uma conexão de rota expressa criada entre um gateway de rota expressa e a paração do circuito de rota expressa local.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="7b4c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b4c7-104">SYNTAX</span></span>

### <span data-ttu-id="7b4c7-105">ByExpressRouteConnectionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7b4c7-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b4c7-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="7b4c7-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b4c7-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7b4c7-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b4c7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b4c7-108">DESCRIPTION</span></span>
<span data-ttu-id="7b4c7-109">O cmdlet **Set-AzExpressRouteConnection** atualiza uma conexão de rota expressa criada entre um gateway de rota expressa e o peering do circuito de rota expressa local.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="7b4c7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-110">EXAMPLES</span></span>

### <span data-ttu-id="7b4c7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b4c7-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
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

<span data-ttu-id="7b4c7-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um ExpressRouteSite no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7b4c7-113">Um gateway ExpressRoute será criado posteriormente no Hub Virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7b4c7-114">Depois que o gateway for criado, ele será conectado ao peering do circuito ExpressRoute local usando o comando New-AzExpressRouteConnection local.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="7b4c7-115">Em seguida, a conexão é atualizada para ter um RoutingWeight diferente usando o comando Set-AzExpressRouteConnection de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="7b4c7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-116">PARAMETERS</span></span>

### <span data-ttu-id="7b4c7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b4c7-117">-AsJob</span></span>
<span data-ttu-id="7b4c7-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7b4c7-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b4c7-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7b4c7-119">-AuthorizationKey</span></span>
<span data-ttu-id="7b4c7-120">A chave de autorização a ser usada para criar a conexão de gateway ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="7b4c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4c7-121">-DefaultProfile</span></span>
<span data-ttu-id="7b4c7-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b4c7-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7b4c7-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="7b4c7-124">Habilitar a segurança da Internet para essa conexão do Gateway ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7b4c7-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="7b4c7-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="7b4c7-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="7b4c7-126">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b4c7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b4c7-127">-InputObject</span></span>
<span data-ttu-id="7b4c7-128">O objeto ExpressRouteConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b4c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7b4c7-129">-Name</span></span>
<span data-ttu-id="7b4c7-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b4c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b4c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="7b4c7-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b4c7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b4c7-133">-ResourceId</span></span>
<span data-ttu-id="7b4c7-134">A id de recurso do objeto ExpressRouteConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b4c7-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4c7-135">-RoutingConfiguration</span></span>
<span data-ttu-id="7b4c7-136">Configuração de roteamento para essa conexão</span><span class="sxs-lookup"><span data-stu-id="7b4c7-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="7b4c7-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7b4c7-137">-RoutingWeight</span></span>
<span data-ttu-id="7b4c7-138">O peso que precisa ser atribuído a essa conexão para roteamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="7b4c7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b4c7-139">-Confirm</span></span>
<span data-ttu-id="7b4c7-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b4c7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b4c7-141">-WhatIf</span></span>
<span data-ttu-id="7b4c7-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b4c7-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b4c7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4c7-144">CommonParameters</span></span>
<span data-ttu-id="7b4c7-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4c7-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b4c7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4c7-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-147">INPUTS</span></span>

### <span data-ttu-id="7b4c7-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7b4c7-148">System.String</span></span>

### <span data-ttu-id="7b4c7-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7b4c7-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7b4c7-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-150">OUTPUTS</span></span>

### <span data-ttu-id="7b4c7-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7b4c7-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7b4c7-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b4c7-152">NOTES</span></span>

## <span data-ttu-id="7b4c7-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b4c7-153">RELATED LINKS</span></span>

[<span data-ttu-id="7b4c7-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b4c7-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
