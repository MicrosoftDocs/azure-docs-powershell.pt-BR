---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429477"
---
# <span data-ttu-id="23b82-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="23b82-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="23b82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23b82-102">SYNOPSIS</span></span>
<span data-ttu-id="23b82-103">Obtém um recurso do VpnSite do Azure por nome ou lista todos os VpnSites em um ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="23b82-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="23b82-104">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="23b82-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23b82-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23b82-105">SYNTAX</span></span>

### <span data-ttu-id="23b82-106">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="23b82-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23b82-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b82-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23b82-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23b82-108">DESCRIPTION</span></span>
<span data-ttu-id="23b82-109">Obtém um recurso do VpnSite do Azure por nome ou lista todos os VpnSites em um ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="23b82-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="23b82-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23b82-110">EXAMPLES</span></span>

### <span data-ttu-id="23b82-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23b82-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="23b82-112">A seguir, você criará um grupo de recursos, uma WAN virtual no oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="23b82-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="23b82-113">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="23b82-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="23b82-114">Depois que o site for criado, ele receberá o site usando o comando Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="23b82-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="23b82-115">OS</span><span class="sxs-lookup"><span data-stu-id="23b82-115">PARAMETERS</span></span>

### <span data-ttu-id="23b82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b82-116">-DefaultProfile</span></span>
<span data-ttu-id="23b82-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23b82-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b82-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="23b82-118">-Name</span></span>
<span data-ttu-id="23b82-119">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="23b82-119">The resource name.</span></span>

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

### <span data-ttu-id="23b82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b82-120">-ResourceGroupName</span></span>
<span data-ttu-id="23b82-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23b82-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b82-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b82-122">CommonParameters</span></span>
<span data-ttu-id="23b82-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b82-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b82-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b82-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b82-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23b82-125">INPUTS</span></span>

### <span data-ttu-id="23b82-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="23b82-126">None</span></span>

## <span data-ttu-id="23b82-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23b82-127">OUTPUTS</span></span>

### <span data-ttu-id="23b82-128">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="23b82-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="23b82-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23b82-129">NOTES</span></span>

## <span data-ttu-id="23b82-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23b82-130">RELATED LINKS</span></span>
