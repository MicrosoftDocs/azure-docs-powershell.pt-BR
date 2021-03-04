---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889433"
---
# <span data-ttu-id="51cdd-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="51cdd-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="51cdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="51cdd-103">Cria um Gateway VPN escalonável.</span><span class="sxs-lookup"><span data-stu-id="51cdd-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="51cdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51cdd-104">SYNTAX</span></span>

### <span data-ttu-id="51cdd-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51cdd-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51cdd-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="51cdd-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51cdd-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="51cdd-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51cdd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51cdd-108">DESCRIPTION</span></span>
<span data-ttu-id="51cdd-109">New-AzVpnGateway cria um Gateway VPN escalonável.</span><span class="sxs-lookup"><span data-stu-id="51cdd-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="51cdd-110">Essa é a conectividade definida pelo software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="51cdd-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="51cdd-111">Esse gateway resize e dimensiona com base na unidade de escala especificada neste ou Set-AzVpnGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51cdd-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="51cdd-112">Uma conexão é configurada de um branch/Site conhecido como VPNSite para o gateway escalonável.</span><span class="sxs-lookup"><span data-stu-id="51cdd-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="51cdd-113">Cada conexão é composta por 2 Active-Active túnel.</span><span class="sxs-lookup"><span data-stu-id="51cdd-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="51cdd-114">O VpnGateway estará no mesmo local que o VirtualHub referenciado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="51cdd-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51cdd-115">EXAMPLES</span></span>

### <span data-ttu-id="51cdd-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51cdd-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="51cdd-117">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="51cdd-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="51cdd-118">Um gateway VPN será criado posteriormente no Hub Virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="51cdd-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="51cdd-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51cdd-119">PARAMETERS</span></span>

### <span data-ttu-id="51cdd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51cdd-120">-AsJob</span></span>
<span data-ttu-id="51cdd-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51cdd-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cdd-122">-DefaultProfile</span></span>
<span data-ttu-id="51cdd-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51cdd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51cdd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="51cdd-124">-Name</span></span>
<span data-ttu-id="51cdd-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="51cdd-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51cdd-126">-ResourceGroupName</span></span>
<span data-ttu-id="51cdd-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="51cdd-127">The resource name.</span></span>

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

### <span data-ttu-id="51cdd-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="51cdd-128">-Tag</span></span>
<span data-ttu-id="51cdd-129">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="51cdd-129">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="51cdd-130">-VirtualHub</span></span>
<span data-ttu-id="51cdd-131">O VirtualHub ao que o VpnGateway precisa ser associado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="51cdd-132">-VirtualHubId</span></span>
<span data-ttu-id="51cdd-133">A ID do VirtualHub a que o VpnGateway precisa ser associado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="51cdd-134">-VirtualHubName</span></span>
<span data-ttu-id="51cdd-135">A ID do VirtualHub a que o VpnGateway precisa ser associado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="51cdd-136">-VpnConnection</span></span>
<span data-ttu-id="51cdd-137">A lista de VpnConnections que essa VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="51cdd-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="51cdd-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="51cdd-139">A lista de VpnGatewayNatRules associada a essa VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="51cdd-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="51cdd-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="51cdd-141">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="51cdd-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="51cdd-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="51cdd-143">Sinalizador para habilitar a Internet de Preferência de Roteamento nesta VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="51cdd-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="51cdd-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51cdd-144">-Confirm</span></span>
<span data-ttu-id="51cdd-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51cdd-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cdd-146">-WhatIf</span></span>
<span data-ttu-id="51cdd-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51cdd-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51cdd-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cdd-149">CommonParameters</span></span>
<span data-ttu-id="51cdd-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cdd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cdd-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51cdd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cdd-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51cdd-152">INPUTS</span></span>

### <span data-ttu-id="51cdd-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51cdd-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="51cdd-154">System.String</span><span class="sxs-lookup"><span data-stu-id="51cdd-154">System.String</span></span>
## <span data-ttu-id="51cdd-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51cdd-155">OUTPUTS</span></span>

### <span data-ttu-id="51cdd-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="51cdd-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="51cdd-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="51cdd-157">NOTES</span></span>

## <span data-ttu-id="51cdd-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51cdd-158">RELATED LINKS</span></span>

[<span data-ttu-id="51cdd-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="51cdd-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="51cdd-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="51cdd-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="51cdd-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="51cdd-161">Update-AzVpnGateway</span></span>]()

