---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111589"
---
# <span data-ttu-id="02d11-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="02d11-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="02d11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d11-102">SYNOPSIS</span></span>
<span data-ttu-id="02d11-103">Obtém um recurso do VpnSite do Azure por nome ou lista todos os VpnSites em um ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="02d11-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="02d11-104">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="02d11-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="02d11-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d11-105">SYNTAX</span></span>

### <span data-ttu-id="02d11-106">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="02d11-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02d11-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d11-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02d11-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d11-108">DESCRIPTION</span></span>
<span data-ttu-id="02d11-109">Obtém um recurso do VpnSite do Azure por nome ou lista todos os VpnSites em um ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="02d11-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="02d11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d11-110">EXAMPLES</span></span>

### <span data-ttu-id="02d11-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02d11-111">Example 1</span></span>

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

<span data-ttu-id="02d11-112">A seguir, você criará um grupo de recursos, uma WAN virtual no oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="02d11-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="02d11-113">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="02d11-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="02d11-114">Depois que o site for criado, ele receberá o site usando o comando Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="02d11-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="02d11-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="02d11-115">Example 2</span></span>

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

<span data-ttu-id="02d11-116">Este cmdlet obtém todos os sites que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="02d11-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="02d11-117">OS</span><span class="sxs-lookup"><span data-stu-id="02d11-117">PARAMETERS</span></span>

### <span data-ttu-id="02d11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d11-118">-DefaultProfile</span></span>
<span data-ttu-id="02d11-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02d11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d11-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d11-120">-Name</span></span>
<span data-ttu-id="02d11-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="02d11-121">The resource name.</span></span>

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

### <span data-ttu-id="02d11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d11-122">-ResourceGroupName</span></span>
<span data-ttu-id="02d11-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02d11-123">The resource group name.</span></span>

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

### <span data-ttu-id="02d11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d11-124">CommonParameters</span></span>
<span data-ttu-id="02d11-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d11-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02d11-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d11-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d11-127">INPUTS</span></span>

### <span data-ttu-id="02d11-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02d11-128">None</span></span>

## <span data-ttu-id="02d11-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d11-129">OUTPUTS</span></span>

### <span data-ttu-id="02d11-130">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="02d11-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="02d11-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d11-131">NOTES</span></span>

## <span data-ttu-id="02d11-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d11-132">RELATED LINKS</span></span>

[<span data-ttu-id="02d11-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="02d11-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="02d11-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="02d11-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="02d11-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="02d11-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
