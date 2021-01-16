---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260236"
---
# <span data-ttu-id="86112-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86112-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="86112-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86112-102">SYNOPSIS</span></span>
<span data-ttu-id="86112-103">Cria um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="86112-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="86112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86112-104">SYNTAX</span></span>

### <span data-ttu-id="86112-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="86112-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86112-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="86112-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86112-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="86112-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86112-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86112-108">DESCRIPTION</span></span>

<span data-ttu-id="86112-109">New-AzVpnGateway cria um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="86112-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="86112-110">Esta é uma conectividade definida por software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="86112-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="86112-111">Esse gateway é redimensionado e dimensionado com base na unidade de escala especificada neste cmdlet Set-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="86112-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="86112-112">Uma conexão é configurada a partir de uma ramificação/site conhecida como VPNSite ao gateway expansível.</span><span class="sxs-lookup"><span data-stu-id="86112-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="86112-113">Cada conexão é composta por 2 Active-Active túneis.</span><span class="sxs-lookup"><span data-stu-id="86112-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="86112-114">O VpnGateway estará no mesmo local do VirtualHub referenciado.</span><span class="sxs-lookup"><span data-stu-id="86112-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="86112-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86112-115">EXAMPLES</span></span>

### <span data-ttu-id="86112-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86112-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="86112-117">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="86112-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="86112-118">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="86112-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="86112-119">OS</span><span class="sxs-lookup"><span data-stu-id="86112-119">PARAMETERS</span></span>

### <span data-ttu-id="86112-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86112-120">-AsJob</span></span>
<span data-ttu-id="86112-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="86112-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86112-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86112-122">-DefaultProfile</span></span>
<span data-ttu-id="86112-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86112-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86112-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="86112-124">-Name</span></span>
<span data-ttu-id="86112-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="86112-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86112-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86112-126">-ResourceGroupName</span></span>
<span data-ttu-id="86112-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="86112-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86112-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="86112-128">-Tag</span></span>
<span data-ttu-id="86112-129">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="86112-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="86112-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="86112-130">-VirtualHub</span></span>
<span data-ttu-id="86112-131">O VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="86112-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86112-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="86112-132">-VirtualHubId</span></span>
<span data-ttu-id="86112-133">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="86112-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86112-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="86112-134">-VirtualHubName</span></span>
<span data-ttu-id="86112-135">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="86112-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86112-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="86112-136">-VpnConnection</span></span>
<span data-ttu-id="86112-137">A lista de VpnConnections que esse VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="86112-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="86112-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="86112-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="86112-139">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="86112-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86112-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86112-140">-Confirm</span></span>
<span data-ttu-id="86112-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86112-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86112-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86112-142">-WhatIf</span></span>
<span data-ttu-id="86112-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86112-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86112-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86112-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86112-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86112-145">CommonParameters</span></span>
<span data-ttu-id="86112-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86112-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86112-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86112-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86112-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86112-148">INPUTS</span></span>

### <span data-ttu-id="86112-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86112-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="86112-150">System. String</span><span class="sxs-lookup"><span data-stu-id="86112-150">System.String</span></span>

## <span data-ttu-id="86112-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86112-151">OUTPUTS</span></span>

### <span data-ttu-id="86112-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86112-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="86112-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86112-153">NOTES</span></span>

## <span data-ttu-id="86112-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86112-154">RELATED LINKS</span></span>

[<span data-ttu-id="86112-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86112-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="86112-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86112-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="86112-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86112-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
