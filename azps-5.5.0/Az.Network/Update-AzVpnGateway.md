---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: b38108a9655378349efff44bae3e51efc3ce1f7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113417"
---
# <span data-ttu-id="39bb0-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="39bb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="39bb0-103">Atualiza um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="39bb0-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="39bb0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39bb0-104">SYNTAX</span></span>

### <span data-ttu-id="39bb0-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="39bb0-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bb0-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="39bb0-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bb0-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="39bb0-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39bb0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="39bb0-108">DESCRIPTION</span></span>
<span data-ttu-id="39bb0-109">O cmdlet **Update-AzVpnGateway** atualiza um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="39bb0-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="39bb0-110">Um gateway VPN do Azure é uma conectividade definida pelo software para conexões de site com sites dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="39bb0-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="39bb0-111">Esse gateway é re dimensionado com base na unidade de escala especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="39bb0-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="39bb0-112">Uma conexão pode ser configurada de uma ramificação/site conhecido como site VPN para o gateway escalável.</span><span class="sxs-lookup"><span data-stu-id="39bb0-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="39bb0-113">Cada conexão é composta por 2 Active-Active túnel</span><span class="sxs-lookup"><span data-stu-id="39bb0-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="39bb0-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="39bb0-114">EXAMPLES</span></span>

### <span data-ttu-id="39bb0-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39bb0-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="39bb0-116">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="39bb0-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="39bb0-117">Um gateway VPN será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="39bb0-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="39bb0-118">Depois que o gateway é criado, ele usa Update-AzVpnGateway atualizar o gateway para 3 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="39bb0-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="39bb0-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="39bb0-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="39bb0-120">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="39bb0-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="39bb0-121">Um gateway VPN será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="39bb0-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="39bb0-122">Depois que o gateway for criado, ele será Set-AzVpnGateway atualizar bgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="39bb0-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="39bb0-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39bb0-123">PARAMETERS</span></span>

### <span data-ttu-id="39bb0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39bb0-124">-AsJob</span></span>
<span data-ttu-id="39bb0-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="39bb0-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39bb0-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="39bb0-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="39bb0-127">Os endereços de par BGP para os bgpsettings do VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="39bb0-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bb0-128">-DefaultProfile</span></span>
<span data-ttu-id="39bb0-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39bb0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bb0-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39bb0-130">-InputObject</span></span>
<span data-ttu-id="39bb0-131">O objeto de gateway vpn a ser modificado</span><span class="sxs-lookup"><span data-stu-id="39bb0-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="39bb0-132">-Name</span></span>
<span data-ttu-id="39bb0-133">O nome do gateway vpn.</span><span class="sxs-lookup"><span data-stu-id="39bb0-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bb0-134">-ResourceGroupName</span></span>
<span data-ttu-id="39bb0-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39bb0-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39bb0-136">-ResourceId</span></span>
<span data-ttu-id="39bb0-137">A ID de recurso do Azure do VpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="39bb0-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="39bb0-138">-Tag</span></span>
<span data-ttu-id="39bb0-139">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="39bb0-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39bb0-140">-VpnConnection</span></span>
<span data-ttu-id="39bb0-141">A lista de VpnConnections que este VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="39bb0-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bb0-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="39bb0-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="39bb0-143">A lista de VpnGatewayNatRules associada a este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="39bb0-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="39bb0-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="39bb0-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="39bb0-145">A unidade de escala deste VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="39bb0-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="39bb0-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="39bb0-146">-Confirm</span></span>
<span data-ttu-id="39bb0-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39bb0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bb0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bb0-148">-WhatIf</span></span>
<span data-ttu-id="39bb0-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="39bb0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bb0-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39bb0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bb0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bb0-151">CommonParameters</span></span>
<span data-ttu-id="39bb0-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bb0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bb0-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39bb0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bb0-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="39bb0-154">INPUTS</span></span>

### <span data-ttu-id="39bb0-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="39bb0-156">System.String</span><span class="sxs-lookup"><span data-stu-id="39bb0-156">System.String</span></span>

## <span data-ttu-id="39bb0-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="39bb0-157">OUTPUTS</span></span>

### <span data-ttu-id="39bb0-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="39bb0-159">Notas</span><span class="sxs-lookup"><span data-stu-id="39bb0-159">NOTES</span></span>

## <span data-ttu-id="39bb0-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39bb0-160">RELATED LINKS</span></span>

[<span data-ttu-id="39bb0-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="39bb0-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="39bb0-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="39bb0-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)