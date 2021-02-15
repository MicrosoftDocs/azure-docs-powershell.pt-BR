---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115104"
---
# <span data-ttu-id="d2593-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2593-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="d2593-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2593-102">SYNOPSIS</span></span>
<span data-ttu-id="d2593-103">Cria um objeto Tabela de Rota do Hub Virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2593-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="d2593-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2593-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2593-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2593-105">DESCRIPTION</span></span>
<span data-ttu-id="d2593-106">Cria um objeto Tabela de Rota do Hub Virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2593-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="d2593-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2593-107">EXAMPLES</span></span>

### <span data-ttu-id="d2593-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2593-108">Example 1</span></span>

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

<span data-ttu-id="d2593-109">A tabela de rota acima criará uma tabela composta por várias rotas e anexada a um novo hub virtual.</span><span class="sxs-lookup"><span data-stu-id="d2593-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="d2593-110">Esse é um objeto na memória que pode ser usado para adicionar uma tabela De roteamento a um Novo ou a um VirtualHub existente.</span><span class="sxs-lookup"><span data-stu-id="d2593-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="d2593-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2593-111">PARAMETERS</span></span>

### <span data-ttu-id="d2593-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2593-112">-DefaultProfile</span></span>
<span data-ttu-id="d2593-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2593-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2593-114">-Rota</span><span class="sxs-lookup"><span data-stu-id="d2593-114">-Route</span></span>
<span data-ttu-id="d2593-115">Lista de rotas do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="d2593-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="d2593-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2593-116">CommonParameters</span></span>
<span data-ttu-id="d2593-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2593-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2593-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2593-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2593-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2593-119">INPUTS</span></span>

### <span data-ttu-id="d2593-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d2593-120">None</span></span>

## <span data-ttu-id="d2593-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2593-121">OUTPUTS</span></span>

### <span data-ttu-id="d2593-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2593-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="d2593-123">Notas</span><span class="sxs-lookup"><span data-stu-id="d2593-123">NOTES</span></span>

## <span data-ttu-id="d2593-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2593-124">RELATED LINKS</span></span>

[<span data-ttu-id="d2593-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d2593-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
