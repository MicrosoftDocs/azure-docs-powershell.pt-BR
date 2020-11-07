---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941015"
---
# <span data-ttu-id="3371a-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3371a-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="3371a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3371a-102">SYNOPSIS</span></span>
<span data-ttu-id="3371a-103">Cria um objeto VpnSiteLink do Azure.</span><span class="sxs-lookup"><span data-stu-id="3371a-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="3371a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3371a-104">SYNTAX</span></span>

### <span data-ttu-id="3371a-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="3371a-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3371a-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="3371a-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3371a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3371a-107">DESCRIPTION</span></span>
<span data-ttu-id="3371a-108">Cria um objeto VpnSiteLink do Azure.</span><span class="sxs-lookup"><span data-stu-id="3371a-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="3371a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3371a-109">EXAMPLES</span></span>

### <span data-ttu-id="3371a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3371a-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="3371a-111">A seguir, você criará um grupo de recursos, uma WAN virtual e uma VpnSite com 1 VpnSiteLinks nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="3371a-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="3371a-112">OS</span><span class="sxs-lookup"><span data-stu-id="3371a-112">PARAMETERS</span></span>

### <span data-ttu-id="3371a-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="3371a-113">-BGPAsn</span></span>
<span data-ttu-id="3371a-114">A ASN do BGP para este VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="3371a-114">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="3371a-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3371a-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="3371a-116">O endereço de emparelhamento BGP para este VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="3371a-116">The BGP Peering Address for this VpnSiteLink.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3371a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3371a-117">-DefaultProfile</span></span>
<span data-ttu-id="3371a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3371a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3371a-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="3371a-119">-Fqdn</span></span>
<span data-ttu-id="3371a-120">O próximo salto FQDN.</span><span class="sxs-lookup"><span data-stu-id="3371a-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3371a-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3371a-121">-IPAddress</span></span>
<span data-ttu-id="3371a-122">O endereço IP do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3371a-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3371a-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="3371a-123">-LinkProviderName</span></span>
<span data-ttu-id="3371a-124">Nome do provedor do link.</span><span class="sxs-lookup"><span data-stu-id="3371a-124">Link Provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3371a-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="3371a-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="3371a-126">Velocidade do link em Mbps.</span><span class="sxs-lookup"><span data-stu-id="3371a-126">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="3371a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3371a-127">-Name</span></span>
<span data-ttu-id="3371a-128">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="3371a-128">Name</span></span>

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

### <span data-ttu-id="3371a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3371a-129">CommonParameters</span></span>
<span data-ttu-id="3371a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3371a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3371a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3371a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3371a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3371a-132">INPUTS</span></span>

### <span data-ttu-id="3371a-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3371a-133">None</span></span>

## <span data-ttu-id="3371a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3371a-134">OUTPUTS</span></span>

### <span data-ttu-id="3371a-135">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3371a-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="3371a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3371a-136">NOTES</span></span>

## <span data-ttu-id="3371a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3371a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3371a-138">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3371a-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)