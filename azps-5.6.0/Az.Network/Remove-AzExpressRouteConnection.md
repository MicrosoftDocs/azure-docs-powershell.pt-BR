---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 3e9bd0022215f353388e19edb4f5cc6944acbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890778"
---
# <span data-ttu-id="4d511-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4d511-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="4d511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d511-102">SYNOPSIS</span></span>
<span data-ttu-id="4d511-103">Remove um ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4d511-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="4d511-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d511-104">SYNTAX</span></span>

### <span data-ttu-id="4d511-105">ByExpressRouteConnectionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d511-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d511-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="4d511-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d511-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4d511-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d511-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d511-108">DESCRIPTION</span></span>
<span data-ttu-id="4d511-109">Remove um ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4d511-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="4d511-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d511-110">EXAMPLES</span></span>

### <span data-ttu-id="4d511-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d511-111">Example 1</span></span>
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

<span data-ttu-id="4d511-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="4d511-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4d511-113">Um gateway ExpressRoute será criado posteriormente no Hub Virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="4d511-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4d511-114">Depois que o gateway for criado, ele será conectado ao ExpressRouteSite usando o comando New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4d511-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="4d511-115">Em seguida, ele remove a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="4d511-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="4d511-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4d511-116">Example 2</span></span>

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

<span data-ttu-id="4d511-117">O mesmo que o exemplo 1, mas agora remove a conexão usando o objeto canal do Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4d511-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="4d511-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d511-118">PARAMETERS</span></span>

### <span data-ttu-id="4d511-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d511-119">-DefaultProfile</span></span>
<span data-ttu-id="4d511-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d511-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d511-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="4d511-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="4d511-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4d511-122">The parent resource name.</span></span>

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

### <span data-ttu-id="4d511-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4d511-123">-Force</span></span>
<span data-ttu-id="4d511-124">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="4d511-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4d511-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d511-125">-InputObject</span></span>
<span data-ttu-id="4d511-126">O objeto ExpressRouteConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4d511-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="4d511-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4d511-127">-Name</span></span>
<span data-ttu-id="4d511-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d511-128">The resource name.</span></span>

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

### <span data-ttu-id="4d511-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d511-129">-PassThru</span></span>
<span data-ttu-id="4d511-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4d511-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d511-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4d511-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d511-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d511-132">-ResourceGroupName</span></span>
<span data-ttu-id="4d511-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d511-133">The resource group name.</span></span>

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

### <span data-ttu-id="4d511-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d511-134">-ResourceId</span></span>
<span data-ttu-id="4d511-135">A id de recurso do objeto ExpressRouteConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4d511-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="4d511-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d511-136">-Confirm</span></span>
<span data-ttu-id="4d511-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d511-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d511-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d511-138">-WhatIf</span></span>
<span data-ttu-id="4d511-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d511-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d511-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d511-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d511-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d511-141">CommonParameters</span></span>
<span data-ttu-id="4d511-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d511-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d511-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d511-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d511-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d511-144">INPUTS</span></span>

### <span data-ttu-id="4d511-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4d511-145">System.String</span></span>

### <span data-ttu-id="4d511-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4d511-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="4d511-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d511-147">OUTPUTS</span></span>

### <span data-ttu-id="4d511-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d511-148">System.Boolean</span></span>

## <span data-ttu-id="4d511-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d511-149">NOTES</span></span>

## <span data-ttu-id="4d511-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d511-150">RELATED LINKS</span></span>
