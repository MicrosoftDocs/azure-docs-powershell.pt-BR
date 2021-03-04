---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: e5ada12a6fd55cc882ba5b9ba33c817f7eb4daab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887972"
---
# <span data-ttu-id="4502e-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="4502e-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="4502e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4502e-102">SYNOPSIS</span></span>
<span data-ttu-id="4502e-103">Obtém a configuração vpn para um subconjunto de VpnSites conectados a essa WAN por meio de VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="4502e-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="4502e-104">Carrega a configuração de Vpn gerada para um blob de armazenamento especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="4502e-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="4502e-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4502e-105">SYNTAX</span></span>

### <span data-ttu-id="4502e-106">ByVirtualWanNameByVpnSiteObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4502e-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4502e-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4502e-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4502e-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="4502e-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4502e-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4502e-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4502e-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="4502e-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4502e-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4502e-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4502e-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4502e-112">DESCRIPTION</span></span>
<span data-ttu-id="4502e-113">Obtém a configuração vpn para um subconjunto de VpnSites conectados a essa WAN por meio de VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="4502e-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="4502e-114">Carrega a configuração de Vpn gerada para um blob de armazenamento especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="4502e-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="4502e-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4502e-115">EXAMPLES</span></span>

### <span data-ttu-id="4502e-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4502e-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="4502e-117">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="4502e-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4502e-118">Um gateway VPN será criado posteriormente no Hub Virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="4502e-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4502e-119">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4502e-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="4502e-120">Em seguida, a configuração é baixada usando esse commandlet.</span><span class="sxs-lookup"><span data-stu-id="4502e-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="4502e-121">Se o commandlet for bem-sucedido, a configuração de download será escrita no blob indicado pelo SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="4502e-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="4502e-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4502e-122">PARAMETERS</span></span>

### <span data-ttu-id="4502e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4502e-123">-DefaultProfile</span></span>
<span data-ttu-id="4502e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4502e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4502e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4502e-125">-InputObject</span></span>
<span data-ttu-id="4502e-126">O objeto de site vpn a ser modificado</span><span class="sxs-lookup"><span data-stu-id="4502e-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4502e-127">-Name</span></span>
<span data-ttu-id="4502e-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4502e-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4502e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4502e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4502e-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4502e-131">-ResourceId</span></span>
<span data-ttu-id="4502e-132">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="4502e-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="4502e-133">-StorageSasUrl</span></span>
<span data-ttu-id="4502e-134">A URL do SAS para o local de armazenamento onde a configuração deve ser gerada.</span><span class="sxs-lookup"><span data-stu-id="4502e-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="4502e-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4502e-135">-VpnSite</span></span>
<span data-ttu-id="4502e-136">A lista de IDs de recurso VpnSite para gerar configuração.</span><span class="sxs-lookup"><span data-stu-id="4502e-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="4502e-137">-VpnSiteId</span></span>
<span data-ttu-id="4502e-138">A lista de IDs de recurso VpnSite para gerar configuração.</span><span class="sxs-lookup"><span data-stu-id="4502e-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4502e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4502e-139">-Confirm</span></span>
<span data-ttu-id="4502e-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4502e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4502e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4502e-141">-WhatIf</span></span>
<span data-ttu-id="4502e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4502e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4502e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4502e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4502e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4502e-144">CommonParameters</span></span>
<span data-ttu-id="4502e-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4502e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4502e-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4502e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4502e-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4502e-147">INPUTS</span></span>

### <span data-ttu-id="4502e-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4502e-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="4502e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4502e-149">System.String</span></span>

## <span data-ttu-id="4502e-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4502e-150">OUTPUTS</span></span>

### <span data-ttu-id="4502e-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="4502e-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="4502e-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="4502e-152">NOTES</span></span>

## <span data-ttu-id="4502e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4502e-153">RELATED LINKS</span></span>
