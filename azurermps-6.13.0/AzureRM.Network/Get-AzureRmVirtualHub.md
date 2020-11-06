---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610881"
---
# <span data-ttu-id="90008-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90008-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="90008-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90008-102">SYNOPSIS</span></span>
<span data-ttu-id="90008-103">Obtém um VirtualHub do Azure por nome e ResourceGroupName ou lista todos os hubs virtuais por ResourceGroupName/assinatura.</span><span class="sxs-lookup"><span data-stu-id="90008-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90008-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90008-104">SYNTAX</span></span>

### <span data-ttu-id="90008-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="90008-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90008-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90008-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90008-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90008-107">DESCRIPTION</span></span>
<span data-ttu-id="90008-108">Obtém um VirtualHub do Azure por nome e ResourceGroupName ou lista todos os hubs virtuais por ResourceGroupName/assinatura.</span><span class="sxs-lookup"><span data-stu-id="90008-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="90008-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90008-109">EXAMPLES</span></span>

### <span data-ttu-id="90008-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90008-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="90008-111">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="90008-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="90008-112">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="90008-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="90008-113">Em seguida, ele obtém o Hub virtual usando seu ResourceGroupName e ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="90008-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="90008-114">OS</span><span class="sxs-lookup"><span data-stu-id="90008-114">PARAMETERS</span></span>

### <span data-ttu-id="90008-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90008-115">-DefaultProfile</span></span>
<span data-ttu-id="90008-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90008-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90008-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="90008-117">-Name</span></span>
<span data-ttu-id="90008-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="90008-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90008-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90008-119">-ResourceGroupName</span></span>
<span data-ttu-id="90008-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90008-120">The resource group name.</span></span>

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

### <span data-ttu-id="90008-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90008-121">CommonParameters</span></span>
<span data-ttu-id="90008-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90008-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90008-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90008-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90008-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90008-124">INPUTS</span></span>

### <span data-ttu-id="90008-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="90008-125">None</span></span>

## <span data-ttu-id="90008-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90008-126">OUTPUTS</span></span>

### <span data-ttu-id="90008-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90008-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="90008-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90008-128">NOTES</span></span>

## <span data-ttu-id="90008-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90008-129">RELATED LINKS</span></span>
