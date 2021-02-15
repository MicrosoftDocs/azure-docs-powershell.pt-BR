---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114660"
---
# <span data-ttu-id="cd09a-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cd09a-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="cd09a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd09a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd09a-103">Remove uma Conexão Do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cd09a-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cd09a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd09a-104">SYNTAX</span></span>

### <span data-ttu-id="cd09a-105">ByExpressRouteConnectionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cd09a-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd09a-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="cd09a-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd09a-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cd09a-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd09a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd09a-108">DESCRIPTION</span></span>
<span data-ttu-id="cd09a-109">Remove uma Conexão Do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cd09a-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cd09a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cd09a-110">EXAMPLES</span></span>

### <span data-ttu-id="cd09a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd09a-111">Example 1</span></span>
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

<span data-ttu-id="cd09a-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="cd09a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cd09a-113">Um gateway do ExpressRoute será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="cd09a-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cd09a-114">Depois que o gateway for criado, ele será conectado ao ExpressRouteSite usando o comando New-AzExpressRouteConnection usuário.</span><span class="sxs-lookup"><span data-stu-id="cd09a-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="cd09a-115">Em seguida, ela remove a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="cd09a-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="cd09a-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd09a-116">Example 2</span></span>

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

<span data-ttu-id="cd09a-117">O mesmo que o exemplo 1, mas agora remove a conexão usando o objeto encadeado do Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="cd09a-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="cd09a-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd09a-118">PARAMETERS</span></span>

### <span data-ttu-id="cd09a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd09a-119">-DefaultProfile</span></span>
<span data-ttu-id="cd09a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd09a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd09a-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="cd09a-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="cd09a-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="cd09a-122">The parent resource name.</span></span>

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

### <span data-ttu-id="cd09a-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="cd09a-123">-Force</span></span>
<span data-ttu-id="cd09a-124">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="cd09a-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cd09a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd09a-125">-InputObject</span></span>
<span data-ttu-id="cd09a-126">O objeto ExpressRouteConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cd09a-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="cd09a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd09a-127">-Name</span></span>
<span data-ttu-id="cd09a-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd09a-128">The resource name.</span></span>

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

### <span data-ttu-id="cd09a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd09a-129">-PassThru</span></span>
<span data-ttu-id="cd09a-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cd09a-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd09a-131">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="cd09a-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd09a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd09a-132">-ResourceGroupName</span></span>
<span data-ttu-id="cd09a-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd09a-133">The resource group name.</span></span>

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

### <span data-ttu-id="cd09a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd09a-134">-ResourceId</span></span>
<span data-ttu-id="cd09a-135">A ID do recurso do objeto ExpressRouteConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cd09a-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="cd09a-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cd09a-136">-Confirm</span></span>
<span data-ttu-id="cd09a-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd09a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd09a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd09a-138">-WhatIf</span></span>
<span data-ttu-id="cd09a-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cd09a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd09a-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd09a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd09a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd09a-141">CommonParameters</span></span>
<span data-ttu-id="cd09a-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd09a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd09a-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd09a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd09a-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="cd09a-144">INPUTS</span></span>

### <span data-ttu-id="cd09a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cd09a-145">System.String</span></span>

### <span data-ttu-id="cd09a-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cd09a-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="cd09a-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="cd09a-147">OUTPUTS</span></span>

### <span data-ttu-id="cd09a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd09a-148">System.Boolean</span></span>

## <span data-ttu-id="cd09a-149">Notas</span><span class="sxs-lookup"><span data-stu-id="cd09a-149">NOTES</span></span>

## <span data-ttu-id="cd09a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd09a-150">RELATED LINKS</span></span>
