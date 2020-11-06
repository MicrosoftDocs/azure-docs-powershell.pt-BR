---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 3ccf321a089dbb519293fe6407581aecf32b8157
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600268"
---
# <span data-ttu-id="347a0-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="347a0-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="347a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="347a0-102">SYNOPSIS</span></span>
<span data-ttu-id="347a0-103">Cria um objeto da tabela de rota do Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="347a0-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="347a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="347a0-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="347a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="347a0-105">DESCRIPTION</span></span>
<span data-ttu-id="347a0-106">Cria um objeto da tabela de rota do Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="347a0-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="347a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="347a0-107">EXAMPLES</span></span>

### <span data-ttu-id="347a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="347a0-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="347a0-109">A seguir, você criará uma tabela de rota composta por várias rotas e anexada a um novo hub virtual.</span><span class="sxs-lookup"><span data-stu-id="347a0-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="347a0-110">Esse é um objeto na memória que pode ser usado para adicionar uma tabela de rota a um novo ou a um VirtualHub existente.</span><span class="sxs-lookup"><span data-stu-id="347a0-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="347a0-111">OS</span><span class="sxs-lookup"><span data-stu-id="347a0-111">PARAMETERS</span></span>

### <span data-ttu-id="347a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347a0-112">-DefaultProfile</span></span>
<span data-ttu-id="347a0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="347a0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="347a0-114">-Rota</span><span class="sxs-lookup"><span data-stu-id="347a0-114">-Route</span></span>
<span data-ttu-id="347a0-115">Lista de rotas de Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="347a0-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="347a0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347a0-116">CommonParameters</span></span>
<span data-ttu-id="347a0-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="347a0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347a0-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="347a0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347a0-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="347a0-119">INPUTS</span></span>

### <span data-ttu-id="347a0-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="347a0-120">None</span></span>

## <span data-ttu-id="347a0-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="347a0-121">OUTPUTS</span></span>

### <span data-ttu-id="347a0-122">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="347a0-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="347a0-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="347a0-123">NOTES</span></span>

## <span data-ttu-id="347a0-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="347a0-124">RELATED LINKS</span></span>

[<span data-ttu-id="347a0-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="347a0-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
