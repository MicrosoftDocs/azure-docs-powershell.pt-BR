---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
ms.openlocfilehash: b29b57ea7d7a5182a25cb05ae05e6d1644a5c18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429457"
---
# <span data-ttu-id="a9e43-101">New-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a9e43-101">New-AzureRmVpnGateway</span></span>

## <span data-ttu-id="a9e43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9e43-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e43-103">Cria um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="a9e43-103">Creates a Scalable VPN Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9e43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9e43-104">SYNTAX</span></span>

### <span data-ttu-id="a9e43-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9e43-105">ByVirtualHubName (Default)</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e43-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a9e43-106">ByVirtualHubObject</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e43-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e43-107">ByVirtualHubResourceId</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e43-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9e43-108">DESCRIPTION</span></span>

<span data-ttu-id="a9e43-109">New-AzureRmVpnGateway cria um gateway VPN escalável.</span><span class="sxs-lookup"><span data-stu-id="a9e43-109">New-AzureRmVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="a9e43-110">Esta é uma conectividade definida por software para conexões de site para site dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a9e43-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="a9e43-111">Esse gateway é redimensionado e dimensionado com base na unidade de escala especificada neste cmdlet Set-AzureRmVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a9e43-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzureRmVpnGateway cmdlet.</span></span> 

<span data-ttu-id="a9e43-112">Uma conexão é configurada a partir de uma ramificação/site conhecida como VPNSite ao gateway expansível.</span><span class="sxs-lookup"><span data-stu-id="a9e43-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="a9e43-113">Cada conexão é composta por 2 Active-Active túneis.</span><span class="sxs-lookup"><span data-stu-id="a9e43-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="a9e43-114">O VpnGateway estará no mesmo local do VirtualHub referenciado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="a9e43-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9e43-115">EXAMPLES</span></span>

### <span data-ttu-id="a9e43-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9e43-116">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="a9e43-117">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e43-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a9e43-118">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="a9e43-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="a9e43-119">OS</span><span class="sxs-lookup"><span data-stu-id="a9e43-119">PARAMETERS</span></span>

### <span data-ttu-id="a9e43-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9e43-120">-AsJob</span></span>
<span data-ttu-id="a9e43-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a9e43-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9e43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e43-122">-DefaultProfile</span></span>
<span data-ttu-id="a9e43-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e43-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e43-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9e43-124">-Name</span></span>
<span data-ttu-id="a9e43-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a9e43-125">The resource name.</span></span>

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

### <span data-ttu-id="a9e43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e43-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9e43-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a9e43-127">The resource name.</span></span>

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

### <span data-ttu-id="a9e43-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="a9e43-128">-Tag</span></span>
<span data-ttu-id="a9e43-129">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9e43-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a9e43-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a9e43-130">-VirtualHub</span></span>
<span data-ttu-id="a9e43-131">O VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a9e43-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a9e43-132">-VirtualHubId</span></span>
<span data-ttu-id="a9e43-133">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a9e43-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="a9e43-134">-VirtualHubName</span></span>
<span data-ttu-id="a9e43-135">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a9e43-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a9e43-136">-VpnConnection</span></span>
<span data-ttu-id="a9e43-137">A lista de VpnConnections que esse VpnGateway precisa ter.</span><span class="sxs-lookup"><span data-stu-id="a9e43-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="a9e43-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a9e43-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="a9e43-139">A unidade de escala para este VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a9e43-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="a9e43-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9e43-140">-Confirm</span></span>
<span data-ttu-id="a9e43-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e43-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e43-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e43-142">-WhatIf</span></span>
<span data-ttu-id="a9e43-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e43-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9e43-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e43-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e43-145">CommonParameters</span></span>
<span data-ttu-id="a9e43-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e43-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e43-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e43-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e43-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9e43-148">INPUTS</span></span>

### <span data-ttu-id="a9e43-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a9e43-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a9e43-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e43-150">System.String</span></span>

## <span data-ttu-id="a9e43-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9e43-151">OUTPUTS</span></span>

### <span data-ttu-id="a9e43-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a9e43-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="a9e43-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9e43-153">NOTES</span></span>

## <span data-ttu-id="a9e43-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9e43-154">RELATED LINKS</span></span>
