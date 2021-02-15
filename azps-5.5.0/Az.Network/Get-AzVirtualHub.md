---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117439"
---
# <span data-ttu-id="66edb-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66edb-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="66edb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66edb-102">SYNOPSIS</span></span>
<span data-ttu-id="66edb-103">Obtém um Azure VirtualHub por Nome e ResourceGroupName ou lista todos os Hubs Virtuais por ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="66edb-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="66edb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66edb-104">SYNTAX</span></span>

### <span data-ttu-id="66edb-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66edb-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66edb-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66edb-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66edb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="66edb-107">DESCRIPTION</span></span>
<span data-ttu-id="66edb-108">Obtém um Azure VirtualHub por Nome e ResourceGroupName ou lista todos os Hubs Virtuais por ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="66edb-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="66edb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66edb-109">EXAMPLES</span></span>

### <span data-ttu-id="66edb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66edb-110">Example 1</span></span>

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

<span data-ttu-id="66edb-111">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="66edb-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="66edb-112">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="66edb-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="66edb-113">Em seguida, ele obtém o hub virtual usando o ResourceGroupName e o ResourceName.</span><span class="sxs-lookup"><span data-stu-id="66edb-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="66edb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="66edb-114">Example 2</span></span>

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

<span data-ttu-id="66edb-115">Este cmdlet obtém o hub virtual usando filtragem.</span><span class="sxs-lookup"><span data-stu-id="66edb-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="66edb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66edb-116">PARAMETERS</span></span>

### <span data-ttu-id="66edb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66edb-117">-DefaultProfile</span></span>
<span data-ttu-id="66edb-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66edb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66edb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="66edb-119">-Name</span></span>
<span data-ttu-id="66edb-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="66edb-120">The resource name.</span></span>

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

### <span data-ttu-id="66edb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66edb-121">-ResourceGroupName</span></span>
<span data-ttu-id="66edb-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66edb-122">The resource group name.</span></span>

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

### <span data-ttu-id="66edb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66edb-123">CommonParameters</span></span>
<span data-ttu-id="66edb-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66edb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66edb-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66edb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66edb-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="66edb-126">INPUTS</span></span>

### <span data-ttu-id="66edb-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="66edb-127">None</span></span>

## <span data-ttu-id="66edb-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="66edb-128">OUTPUTS</span></span>

### <span data-ttu-id="66edb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66edb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="66edb-130">Notas</span><span class="sxs-lookup"><span data-stu-id="66edb-130">NOTES</span></span>

## <span data-ttu-id="66edb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66edb-131">RELATED LINKS</span></span>

[<span data-ttu-id="66edb-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66edb-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="66edb-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66edb-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="66edb-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66edb-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
