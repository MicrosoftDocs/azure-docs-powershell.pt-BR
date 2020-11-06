---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600490"
---
# <span data-ttu-id="d1a9c-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1a9c-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="d1a9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a9c-103">Obtém um VirtualHub do Azure por nome e ResourceGroupName ou lista todos os hubs virtuais por ResourceGroupName/assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="d1a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a9c-104">SYNTAX</span></span>

### <span data-ttu-id="d1a9c-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1a9c-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a9c-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a9c-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1a9c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="d1a9c-108">Obtém um VirtualHub do Azure por nome e ResourceGroupName ou lista todos os hubs virtuais por ResourceGroupName/assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="d1a9c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="d1a9c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1a9c-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="d1a9c-111">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="d1a9c-112">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="d1a9c-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="d1a9c-113">Em seguida, ele obtém o Hub virtual usando seu ResourceGroupName e ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="d1a9c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d1a9c-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="d1a9c-115">Este cmdlet obtém o Hub virtual usando a filtragem.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="d1a9c-116">OS</span><span class="sxs-lookup"><span data-stu-id="d1a9c-116">PARAMETERS</span></span>

### <span data-ttu-id="d1a9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a9c-117">-DefaultProfile</span></span>
<span data-ttu-id="d1a9c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a9c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1a9c-119">-Name</span></span>
<span data-ttu-id="d1a9c-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d1a9c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a9c-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1a9c-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d1a9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a9c-123">CommonParameters</span></span>
<span data-ttu-id="d1a9c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a9c-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1a9c-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a9c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1a9c-126">INPUTS</span></span>

### <span data-ttu-id="d1a9c-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d1a9c-127">None</span></span>

## <span data-ttu-id="d1a9c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1a9c-128">OUTPUTS</span></span>

### <span data-ttu-id="d1a9c-129">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1a9c-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="d1a9c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1a9c-130">NOTES</span></span>

## <span data-ttu-id="d1a9c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1a9c-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1a9c-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1a9c-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="d1a9c-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1a9c-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="d1a9c-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1a9c-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
