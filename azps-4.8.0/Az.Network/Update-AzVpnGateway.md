---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114049"
---
# <span data-ttu-id="8a4f9-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="8a4f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4f9-103">Atualiza um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="8a4f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a4f9-104">SYNTAX</span></span>

### <span data-ttu-id="8a4f9-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a4f9-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a4f9-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8a4f9-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a4f9-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4f9-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a4f9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a4f9-108">DESCRIPTION</span></span>
<span data-ttu-id="8a4f9-109">O cmdlet **Update-AzVpnGateway** atualiza um gateway VPN dimensionável.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="8a4f9-110">Um gateway de VPN do Azure é uma conectividade definida por software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="8a4f9-111">Esse gateway é redimensionado e dimensionado com base na unidade de escala especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="8a4f9-112">Uma conexão pode ser configurada de uma filial/site conhecida como site VPN para o gateway escalonável.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="8a4f9-113">Cada conexão compreende 2 Active-Active túneis</span><span class="sxs-lookup"><span data-stu-id="8a4f9-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="8a4f9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a4f9-114">EXAMPLES</span></span>

### <span data-ttu-id="8a4f9-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a4f9-115">Example 1</span></span>

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

<span data-ttu-id="8a4f9-116">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8a4f9-117">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8a4f9-118">Após a criação do gateway, ele usa Update-AzVpnGateway para atualizar o gateway para 3 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="8a4f9-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a4f9-119">Example 2</span></span>

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

<span data-ttu-id="8a4f9-120">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8a4f9-121">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8a4f9-122">Após a criação do gateway, ele usa Set-AzVpnGateway para atualizar o BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="8a4f9-123">OS</span><span class="sxs-lookup"><span data-stu-id="8a4f9-123">PARAMETERS</span></span>

### <span data-ttu-id="8a4f9-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a4f9-124">-AsJob</span></span>
<span data-ttu-id="8a4f9-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a4f9-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a4f9-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="8a4f9-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="8a4f9-127">Os endereços de emparelhamento BGP para este VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f9-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a4f9-128">-Confirm</span></span>
<span data-ttu-id="8a4f9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4f9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4f9-130">-DefaultProfile</span></span>
<span data-ttu-id="8a4f9-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4f9-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4f9-132">-InputObject</span></span>
<span data-ttu-id="8a4f9-133">O objeto de gateway VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="8a4f9-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f9-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a4f9-134">-Name</span></span>
<span data-ttu-id="8a4f9-135">O nome do gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f9-136">-ResourceGroupName</span></span>
<span data-ttu-id="8a4f9-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4f9-138">-ResourceId</span></span>
<span data-ttu-id="8a4f9-139">A ID de recurso do Azure do VpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f9-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="8a4f9-140">-Tag</span></span>
<span data-ttu-id="8a4f9-141">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8a4f9-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8a4f9-142">-VpnConnection</span></span>
<span data-ttu-id="8a4f9-143">A lista de VpnConnections que esse VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="8a4f9-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8a4f9-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="8a4f9-145">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="8a4f9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4f9-146">-WhatIf</span></span>
<span data-ttu-id="8a4f9-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4f9-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4f9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4f9-149">CommonParameters</span></span>
<span data-ttu-id="8a4f9-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4f9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4f9-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4f9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4f9-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a4f9-152">INPUTS</span></span>

### <span data-ttu-id="8a4f9-153">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="8a4f9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4f9-154">System.String</span></span>

## <span data-ttu-id="8a4f9-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a4f9-155">OUTPUTS</span></span>

### <span data-ttu-id="8a4f9-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="8a4f9-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a4f9-157">NOTES</span></span>

## <span data-ttu-id="8a4f9-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a4f9-158">RELATED LINKS</span></span>
[<span data-ttu-id="8a4f9-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="8a4f9-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="8a4f9-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8a4f9-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)