---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 70f349fbb6a97009db4ba11e8de945b0700e3c2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600022"
---
# <span data-ttu-id="a87d9-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a87d9-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a87d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a87d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a87d9-103">Atualiza uma conexão de rota expressa criada entre um gateway de rota expressa e o emparelhamento de circuito de rota expressa no local.</span><span class="sxs-lookup"><span data-stu-id="a87d9-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="a87d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a87d9-104">SYNTAX</span></span>

### <span data-ttu-id="a87d9-105">ByExpressRouteConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a87d9-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87d9-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="a87d9-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87d9-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a87d9-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a87d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a87d9-108">DESCRIPTION</span></span>
<span data-ttu-id="a87d9-109">O cmdlet **set-AzExpressRouteConnection** atualiza uma conexão de rota expressa criada entre um gateway de rota expressa e o emparelhamento de circuito de rota expressa no local.</span><span class="sxs-lookup"><span data-stu-id="a87d9-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="a87d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a87d9-110">EXAMPLES</span></span>

### <span data-ttu-id="a87d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a87d9-111">Example 1</span></span>

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
```

<span data-ttu-id="a87d9-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um ExpressRouteSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="a87d9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a87d9-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="a87d9-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a87d9-114">Após a criação do gateway, ele é conectado ao emparelhamento do circuito do ExpressRoute no local, usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="a87d9-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="a87d9-115">A conexão é atualizada para ter um RoutingWeight diferente usando o comando Set-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="a87d9-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="a87d9-116">OS</span><span class="sxs-lookup"><span data-stu-id="a87d9-116">PARAMETERS</span></span>

### <span data-ttu-id="a87d9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a87d9-117">-AsJob</span></span>
<span data-ttu-id="a87d9-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a87d9-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a87d9-119">-AuthorizationKey</span></span>
<span data-ttu-id="a87d9-120">A chave de autorização a ser usada para criar a conexão do gateway do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a87d9-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="a87d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87d9-121">-DefaultProfile</span></span>
<span data-ttu-id="a87d9-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a87d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a87d9-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a87d9-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a87d9-124">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="a87d9-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a87d9-125">-InputObject</span></span>
<span data-ttu-id="a87d9-126">O objeto ExpressRouteConenction a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a87d9-126">The ExpressRouteConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a87d9-127">-Name</span></span>
<span data-ttu-id="a87d9-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a87d9-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="a87d9-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a87d9-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a87d9-131">-ResourceId</span></span>
<span data-ttu-id="a87d9-132">A ID do recurso do objeto ExpressRouteConenction a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a87d9-132">The resource id of the ExpressRouteConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a87d9-133">-RoutingWeight</span></span>
<span data-ttu-id="a87d9-134">A espessura que precisa ser atribuída a essa conexão para roteamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="a87d9-134">The weight that needs to be assigned to this connection for packet routing.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a87d9-135">-Confirm</span></span>
<span data-ttu-id="a87d9-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87d9-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87d9-137">-WhatIf</span></span>
<span data-ttu-id="a87d9-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a87d9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a87d9-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a87d9-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87d9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87d9-140">CommonParameters</span></span>
<span data-ttu-id="a87d9-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87d9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87d9-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87d9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87d9-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a87d9-143">INPUTS</span></span>

### <span data-ttu-id="a87d9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a87d9-144">System.String</span></span>

### <span data-ttu-id="a87d9-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a87d9-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a87d9-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a87d9-146">OUTPUTS</span></span>

### <span data-ttu-id="a87d9-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a87d9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a87d9-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a87d9-148">NOTES</span></span>

## <span data-ttu-id="a87d9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a87d9-149">RELATED LINKS</span></span>
