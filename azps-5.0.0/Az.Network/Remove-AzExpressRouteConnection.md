---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124460"
---
# <span data-ttu-id="cbd65-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cbd65-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="cbd65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbd65-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd65-103">Remove um ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="cbd65-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cbd65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbd65-104">SYNTAX</span></span>

### <span data-ttu-id="cbd65-105">ByExpressRouteConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbd65-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd65-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd65-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd65-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cbd65-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd65-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbd65-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd65-109">Remove um ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="cbd65-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cbd65-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbd65-110">EXAMPLES</span></span>

### <span data-ttu-id="cbd65-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbd65-111">Example 1</span></span>
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
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="cbd65-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd65-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cbd65-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="cbd65-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cbd65-114">Após a criação do gateway, ele é conectado ao ExpressRouteSite usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="cbd65-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="cbd65-115">Em seguida, ele remove a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="cbd65-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="cbd65-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cbd65-116">Example 2</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="cbd65-117">Mesmo que o exemplo 1, mas agora ele remove a conexão usando o objeto piped do Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="cbd65-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="cbd65-118">OS</span><span class="sxs-lookup"><span data-stu-id="cbd65-118">PARAMETERS</span></span>

### <span data-ttu-id="cbd65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd65-119">-DefaultProfile</span></span>
<span data-ttu-id="cbd65-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd65-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="cbd65-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="cbd65-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="cbd65-122">The parent resource name.</span></span>

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

### <span data-ttu-id="cbd65-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cbd65-123">-Force</span></span>
<span data-ttu-id="cbd65-124">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="cbd65-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cbd65-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd65-125">-InputObject</span></span>
<span data-ttu-id="cbd65-126">O objeto ExpressRouteConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cbd65-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="cbd65-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbd65-127">-Name</span></span>
<span data-ttu-id="cbd65-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbd65-128">The resource name.</span></span>

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

### <span data-ttu-id="cbd65-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbd65-129">-PassThru</span></span>
<span data-ttu-id="cbd65-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cbd65-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbd65-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cbd65-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbd65-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd65-132">-ResourceGroupName</span></span>
<span data-ttu-id="cbd65-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbd65-133">The resource group name.</span></span>

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

### <span data-ttu-id="cbd65-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd65-134">-ResourceId</span></span>
<span data-ttu-id="cbd65-135">A ID do recurso do objeto ExpressRouteConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cbd65-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="cbd65-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbd65-136">-Confirm</span></span>
<span data-ttu-id="cbd65-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbd65-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd65-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd65-138">-WhatIf</span></span>
<span data-ttu-id="cbd65-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbd65-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd65-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbd65-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd65-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd65-141">CommonParameters</span></span>
<span data-ttu-id="cbd65-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd65-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd65-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd65-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd65-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbd65-144">INPUTS</span></span>

### <span data-ttu-id="cbd65-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd65-145">System.String</span></span>

### <span data-ttu-id="cbd65-146">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cbd65-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="cbd65-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbd65-147">OUTPUTS</span></span>

### <span data-ttu-id="cbd65-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbd65-148">System.Boolean</span></span>

## <span data-ttu-id="cbd65-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbd65-149">NOTES</span></span>

## <span data-ttu-id="cbd65-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbd65-150">RELATED LINKS</span></span>
