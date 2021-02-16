---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118302"
---
# <span data-ttu-id="2f899-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f899-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="2f899-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f899-102">SYNOPSIS</span></span>
<span data-ttu-id="2f899-103">Cria um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f899-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="2f899-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f899-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f899-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f899-105">DESCRIPTION</span></span>
<span data-ttu-id="2f899-106">Cria um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f899-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="2f899-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f899-107">EXAMPLES</span></span>

### <span data-ttu-id="2f899-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f899-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="2f899-109">O comando acima criará um objeto RoutingConfiguration que pode ser adicionado a um recurso de conexão.</span><span class="sxs-lookup"><span data-stu-id="2f899-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="2f899-110">As rotas estáticas só são permitidas com um objeto HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="2f899-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="2f899-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f899-111">PARAMETERS</span></span>

### <span data-ttu-id="2f899-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f899-112">-DefaultProfile</span></span>
<span data-ttu-id="2f899-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f899-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f899-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f899-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="2f899-115">A tabela de rota do hub associada a essa configuração de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2f899-115">The hub route table associated with this routing configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f899-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2f899-116">-Id</span></span>
<span data-ttu-id="2f899-117">A lista de IDs de recursos de todas as tabelas de rota do hub para anunciar as rotas para a propriedade PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="2f899-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f899-118">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="2f899-118">-Label</span></span>
<span data-ttu-id="2f899-119">A lista de rótulos da propriedade PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="2f899-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f899-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="2f899-120">-StaticRoute</span></span>
<span data-ttu-id="2f899-121">Lista de rotas que controlam o roteamento do VirtualHub para uma conexão de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2f899-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f899-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f899-122">CommonParameters</span></span>
<span data-ttu-id="2f899-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f899-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f899-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f899-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f899-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="2f899-125">INPUTS</span></span>

### <span data-ttu-id="2f899-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2f899-126">System.String</span></span>

### <span data-ttu-id="2f899-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="2f899-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="2f899-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="2f899-128">OUTPUTS</span></span>

### <span data-ttu-id="2f899-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f899-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="2f899-130">Notas</span><span class="sxs-lookup"><span data-stu-id="2f899-130">NOTES</span></span>

## <span data-ttu-id="2f899-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f899-131">RELATED LINKS</span></span>

[<span data-ttu-id="2f899-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="2f899-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="2f899-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="2f899-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="2f899-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="2f899-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="2f899-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2f899-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="2f899-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2f899-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="2f899-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="2f899-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2f899-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)