---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 10514c693ff349550ee2c751f2a3091a7211a41e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427026"
---
# <span data-ttu-id="ea824-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ea824-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="ea824-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea824-102">SYNOPSIS</span></span>
<span data-ttu-id="ea824-103">Obtém uma conexão do ExpressRoute por nome ou lista todas as conexões do ExpressRoute conectadas a um ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ea824-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="ea824-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea824-104">SYNTAX</span></span>

### <span data-ttu-id="ea824-105">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea824-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea824-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea824-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea824-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea824-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea824-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea824-108">DESCRIPTION</span></span>
<span data-ttu-id="ea824-109">Obtém uma conexão do ExpressRoute por nome ou lista todas as conexões do ExpressRoute conectadas a um ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ea824-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="ea824-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea824-110">EXAMPLES</span></span>

### <span data-ttu-id="ea824-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea824-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
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

<span data-ttu-id="ea824-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um ExpressRouteSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea824-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ea824-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="ea824-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ea824-114">Após a criação do gateway, ele é conectado ao circuito do ExpressRoute no local usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="ea824-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="ea824-115">Em seguida, ele obtém a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="ea824-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="ea824-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea824-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
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

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
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

<span data-ttu-id="ea824-117">Esse comando obterá todas as conexões no ExpressRoute "testExpressRoutegw" que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="ea824-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="ea824-118">OS</span><span class="sxs-lookup"><span data-stu-id="ea824-118">PARAMETERS</span></span>

### <span data-ttu-id="ea824-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea824-119">-DefaultProfile</span></span>
<span data-ttu-id="ea824-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea824-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea824-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="ea824-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="ea824-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="ea824-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea824-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea824-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="ea824-124">O ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="ea824-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea824-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea824-125">-Name</span></span>
<span data-ttu-id="ea824-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ea824-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ea824-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ea824-127">-ParentResourceId</span></span>
<span data-ttu-id="ea824-128">A ID do recurso do ExpressRouteGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="ea824-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea824-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea824-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea824-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea824-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea824-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea824-131">CommonParameters</span></span>
<span data-ttu-id="ea824-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea824-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea824-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea824-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea824-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea824-134">INPUTS</span></span>

### <span data-ttu-id="ea824-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ea824-135">System.String</span></span>

## <span data-ttu-id="ea824-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea824-136">OUTPUTS</span></span>

### <span data-ttu-id="ea824-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ea824-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="ea824-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea824-138">NOTES</span></span>

## <span data-ttu-id="ea824-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea824-139">RELATED LINKS</span></span>
