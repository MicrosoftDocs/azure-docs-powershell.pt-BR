---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 444addf1b7f036ffc4fcaae4a1070b9238c29dc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887096"
---
# <span data-ttu-id="b7c49-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7c49-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="b7c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7c49-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c49-103">Obtém um recurso VpnSite do Azure por nome OU lista todos os VpnSites em um ResourceGroup ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="b7c49-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="b7c49-104">Esta é uma representação rm de filiais do cliente que são carregadas para a conectividade do Azure para S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="b7c49-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="b7c49-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7c49-105">SYNTAX</span></span>

### <span data-ttu-id="b7c49-106">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7c49-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c49-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c49-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7c49-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7c49-108">DESCRIPTION</span></span>
<span data-ttu-id="b7c49-109">Obtém um recurso VpnSite do Azure por nome OU lista todos os VpnSites em um ResourceGroup ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="b7c49-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="b7c49-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7c49-110">EXAMPLES</span></span>

### <span data-ttu-id="b7c49-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7c49-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="b7c49-112">O acima criará um grupo de recursos, a WAN Virtual no Oeste dos EUA, no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c49-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="b7c49-113">Em seguida, ele cria um VpnSite para representar uma filial de cliente e o vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="b7c49-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="b7c49-114">Depois que o site é criado, ele obtém o site usando o Get-AzVpnSite comando.</span><span class="sxs-lookup"><span data-stu-id="b7c49-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="b7c49-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7c49-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="b7c49-116">Este cmdlet obtém todos os Sites que começam com "test".</span><span class="sxs-lookup"><span data-stu-id="b7c49-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="b7c49-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7c49-117">PARAMETERS</span></span>

### <span data-ttu-id="b7c49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c49-118">-DefaultProfile</span></span>
<span data-ttu-id="b7c49-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c49-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c49-120">-Name</span></span>
<span data-ttu-id="b7c49-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b7c49-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c49-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7c49-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7c49-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c49-124">CommonParameters</span></span>
<span data-ttu-id="b7c49-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c49-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7c49-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c49-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7c49-127">INPUTS</span></span>

### <span data-ttu-id="b7c49-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7c49-128">None</span></span>

## <span data-ttu-id="b7c49-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7c49-129">OUTPUTS</span></span>

### <span data-ttu-id="b7c49-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7c49-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="b7c49-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7c49-131">NOTES</span></span>

## <span data-ttu-id="b7c49-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7c49-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7c49-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7c49-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="b7c49-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7c49-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="b7c49-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b7c49-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
