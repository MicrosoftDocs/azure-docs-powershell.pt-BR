---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 306bd7262347219afac3ec94ad59dafef579ff94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772685"
---
# <span data-ttu-id="aa17c-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="aa17c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa17c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa17c-103">Atualiza um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="aa17c-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="aa17c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa17c-104">SYNTAX</span></span>

### <span data-ttu-id="aa17c-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa17c-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa17c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="aa17c-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa17c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="aa17c-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa17c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa17c-108">DESCRIPTION</span></span>
<span data-ttu-id="aa17c-109">O cmdlet **Update-AzVpnGateway** atualiza um gateway VPN dimensionável.</span><span class="sxs-lookup"><span data-stu-id="aa17c-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="aa17c-110">Um gateway de VPN do Azure é uma conectividade definida por software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="aa17c-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="aa17c-111">Esse gateway é redimensionado e dimensionado com base na unidade de escala especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aa17c-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="aa17c-112">Uma conexão pode ser configurada de uma filial/site conhecida como site VPN para o gateway escalonável.</span><span class="sxs-lookup"><span data-stu-id="aa17c-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="aa17c-113">Cada conexão compreende 2 Active-Active túneis</span><span class="sxs-lookup"><span data-stu-id="aa17c-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="aa17c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa17c-114">EXAMPLES</span></span>

### <span data-ttu-id="aa17c-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa17c-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="aa17c-116">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa17c-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="aa17c-117">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="aa17c-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="aa17c-118">Após a criação do gateway, ele usa Set-AzVpnGateway para atualizar o gateway para 3 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="aa17c-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="aa17c-119">OS</span><span class="sxs-lookup"><span data-stu-id="aa17c-119">PARAMETERS</span></span>

### <span data-ttu-id="aa17c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa17c-120">-AsJob</span></span>
<span data-ttu-id="aa17c-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa17c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa17c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa17c-122">-DefaultProfile</span></span>
<span data-ttu-id="aa17c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa17c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa17c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa17c-124">-InputObject</span></span>
<span data-ttu-id="aa17c-125">O objeto de gateway VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="aa17c-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="aa17c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa17c-126">-Name</span></span>
<span data-ttu-id="aa17c-127">O nome da rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="aa17c-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="aa17c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa17c-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa17c-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa17c-129">The resource group name.</span></span>

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

### <span data-ttu-id="aa17c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa17c-130">-ResourceId</span></span>
<span data-ttu-id="aa17c-131">A ID de recurso do Azure do VpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="aa17c-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="aa17c-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="aa17c-132">-Tag</span></span>
<span data-ttu-id="aa17c-133">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa17c-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="aa17c-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="aa17c-134">-VpnConnection</span></span>
<span data-ttu-id="aa17c-135">A lista de VpnConnections que esse VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="aa17c-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="aa17c-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="aa17c-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="aa17c-137">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="aa17c-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="aa17c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa17c-138">-Confirm</span></span>
<span data-ttu-id="aa17c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa17c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa17c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa17c-140">-WhatIf</span></span>
<span data-ttu-id="aa17c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa17c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa17c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa17c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa17c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa17c-143">CommonParameters</span></span>
<span data-ttu-id="aa17c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa17c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa17c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa17c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa17c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa17c-146">INPUTS</span></span>

### <span data-ttu-id="aa17c-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="aa17c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="aa17c-148">System.String</span></span>

## <span data-ttu-id="aa17c-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa17c-149">OUTPUTS</span></span>

### <span data-ttu-id="aa17c-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="aa17c-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa17c-151">NOTES</span></span>

## <span data-ttu-id="aa17c-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa17c-152">RELATED LINKS</span></span>

[<span data-ttu-id="aa17c-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="aa17c-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="aa17c-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa17c-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
