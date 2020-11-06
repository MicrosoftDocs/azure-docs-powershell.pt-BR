---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429494"
---
# <span data-ttu-id="24ff0-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="24ff0-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="24ff0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="24ff0-103">Obtém a configuração da VPN para um subconjunto de VpnSites conectado a essa WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="24ff0-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="24ff0-104">Carrega a configuração de VPN gerada para um blob de armazenamento especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="24ff0-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ff0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24ff0-105">SYNTAX</span></span>

### <span data-ttu-id="24ff0-106">ByVirtualWanNameByVpnSiteObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="24ff0-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ff0-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="24ff0-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ff0-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="24ff0-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ff0-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="24ff0-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ff0-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="24ff0-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ff0-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="24ff0-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24ff0-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24ff0-112">DESCRIPTION</span></span>
<span data-ttu-id="24ff0-113">Obtém a configuração da VPN para um subconjunto de VpnSites conectado a essa WAN via VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="24ff0-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="24ff0-114">Carrega a configuração de VPN gerada para um blob de armazenamento especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="24ff0-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="24ff0-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24ff0-115">EXAMPLES</span></span>

### <span data-ttu-id="24ff0-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24ff0-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="24ff0-117">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="24ff0-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="24ff0-118">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="24ff0-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="24ff0-119">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="24ff0-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="24ff0-120">A configuração é então baixada usando o commandlet.</span><span class="sxs-lookup"><span data-stu-id="24ff0-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="24ff0-121">Se o commandlet for bem-sucedido, a configuração de download será gravada no blob indicado pela SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="24ff0-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="24ff0-122">OS</span><span class="sxs-lookup"><span data-stu-id="24ff0-122">PARAMETERS</span></span>

### <span data-ttu-id="24ff0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ff0-123">-DefaultProfile</span></span>
<span data-ttu-id="24ff0-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24ff0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ff0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24ff0-125">-InputObject</span></span>
<span data-ttu-id="24ff0-126">O objeto de site VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="24ff0-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="24ff0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="24ff0-127">-Name</span></span>
<span data-ttu-id="24ff0-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="24ff0-128">The resource name.</span></span>

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

### <span data-ttu-id="24ff0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ff0-129">-ResourceGroupName</span></span>
<span data-ttu-id="24ff0-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24ff0-130">The resource group name.</span></span>

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

### <span data-ttu-id="24ff0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24ff0-131">-ResourceId</span></span>
<span data-ttu-id="24ff0-132">A ID de recurso do Azure para a rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="24ff0-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="24ff0-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="24ff0-133">-StorageSasUrl</span></span>
<span data-ttu-id="24ff0-134">A URL SAS para o local de armazenamento em que a configuração será gerada.</span><span class="sxs-lookup"><span data-stu-id="24ff0-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="24ff0-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="24ff0-135">-VpnSite</span></span>
<span data-ttu-id="24ff0-136">A lista de IDs de recursos de VpnSite para as quais gerar a configuração.</span><span class="sxs-lookup"><span data-stu-id="24ff0-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="24ff0-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="24ff0-137">-VpnSiteId</span></span>
<span data-ttu-id="24ff0-138">A lista de IDs de recursos de VpnSite para as quais gerar a configuração.</span><span class="sxs-lookup"><span data-stu-id="24ff0-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="24ff0-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24ff0-139">-Confirm</span></span>
<span data-ttu-id="24ff0-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ff0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ff0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ff0-141">-WhatIf</span></span>
<span data-ttu-id="24ff0-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24ff0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ff0-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24ff0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ff0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ff0-144">CommonParameters</span></span>
<span data-ttu-id="24ff0-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ff0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ff0-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ff0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ff0-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24ff0-147">INPUTS</span></span>

### <span data-ttu-id="24ff0-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="24ff0-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="24ff0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24ff0-149">System.String</span></span>

## <span data-ttu-id="24ff0-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24ff0-150">OUTPUTS</span></span>

### <span data-ttu-id="24ff0-151">Microsoft. Azure. Commands. Network. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="24ff0-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="24ff0-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24ff0-152">NOTES</span></span>

## <span data-ttu-id="24ff0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24ff0-153">RELATED LINKS</span></span>