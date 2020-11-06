---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602912"
---
# <span data-ttu-id="46ef1-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46ef1-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="46ef1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="46ef1-103">Update-AzureRmVpnGateway atualiza um gateway VPN escalável para o estado de meta apropriado.</span><span class="sxs-lookup"><span data-stu-id="46ef1-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ef1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46ef1-104">SYNTAX</span></span>

### <span data-ttu-id="46ef1-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="46ef1-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46ef1-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="46ef1-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46ef1-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="46ef1-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ef1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46ef1-108">DESCRIPTION</span></span>
<span data-ttu-id="46ef1-109">Update-AzureRmVpnGateway atualiza um gateway VPN escalável para o estado de meta apropriado.</span><span class="sxs-lookup"><span data-stu-id="46ef1-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="46ef1-110">Um AzureRmVpnGateway é uma conectividade definida por software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="46ef1-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="46ef1-111">Esse gateway é redimensionado e dimensionado com base na unidade de escala especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="46ef1-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="46ef1-112">Uma conexão pode ser configurada a partir de um site/filial conhecido como VPNSite para o gateway expansível.</span><span class="sxs-lookup"><span data-stu-id="46ef1-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="46ef1-113">Cada conexão compreende 2 Active-Active túneis</span><span class="sxs-lookup"><span data-stu-id="46ef1-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="46ef1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46ef1-114">EXAMPLES</span></span>

### <span data-ttu-id="46ef1-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46ef1-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="46ef1-116">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="46ef1-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="46ef1-117">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="46ef1-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="46ef1-118">Após a criação do gateway, ele usa Set-AzureRmVpnGateway para atualizar o gateway para 3 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="46ef1-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="46ef1-119">OS</span><span class="sxs-lookup"><span data-stu-id="46ef1-119">PARAMETERS</span></span>

### <span data-ttu-id="46ef1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46ef1-120">-AsJob</span></span>
<span data-ttu-id="46ef1-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46ef1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46ef1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ef1-122">-DefaultProfile</span></span>
<span data-ttu-id="46ef1-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46ef1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ef1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46ef1-124">-InputObject</span></span>
<span data-ttu-id="46ef1-125">O objeto de gateway VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="46ef1-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="46ef1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="46ef1-126">-Name</span></span>
<span data-ttu-id="46ef1-127">O nome da rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="46ef1-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="46ef1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ef1-128">-ResourceGroupName</span></span>
<span data-ttu-id="46ef1-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46ef1-129">The resource group name.</span></span>

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

### <span data-ttu-id="46ef1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46ef1-130">-ResourceId</span></span>
<span data-ttu-id="46ef1-131">A ID de recurso do Azure do VpnGateway a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="46ef1-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="46ef1-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="46ef1-132">-Tag</span></span>
<span data-ttu-id="46ef1-133">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="46ef1-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="46ef1-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46ef1-134">-VpnConnection</span></span>
<span data-ttu-id="46ef1-135">A lista de VpnConnections que esse VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="46ef1-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="46ef1-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="46ef1-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="46ef1-137">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="46ef1-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="46ef1-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46ef1-138">-Confirm</span></span>
<span data-ttu-id="46ef1-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46ef1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ef1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ef1-140">-WhatIf</span></span>
<span data-ttu-id="46ef1-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46ef1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ef1-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46ef1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ef1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ef1-143">CommonParameters</span></span>
<span data-ttu-id="46ef1-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ef1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ef1-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ef1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ef1-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46ef1-146">INPUTS</span></span>

### <span data-ttu-id="46ef1-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46ef1-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="46ef1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="46ef1-148">System.String</span></span>

## <span data-ttu-id="46ef1-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46ef1-149">OUTPUTS</span></span>

### <span data-ttu-id="46ef1-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46ef1-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="46ef1-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46ef1-151">NOTES</span></span>

## <span data-ttu-id="46ef1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46ef1-152">RELATED LINKS</span></span>
