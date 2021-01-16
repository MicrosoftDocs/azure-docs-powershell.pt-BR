---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429556"
---
# <span data-ttu-id="7a60e-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="7a60e-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="7a60e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a60e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a60e-103">Cria um objeto VHubRoute que pode ser passado como parâmetro para o comando New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7a60e-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="7a60e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a60e-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a60e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a60e-105">DESCRIPTION</span></span>

<span data-ttu-id="7a60e-106">Cria um objeto VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="7a60e-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="7a60e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a60e-107">EXAMPLES</span></span>

### <span data-ttu-id="7a60e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a60e-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="7a60e-109">O comando acima criará um objeto VHubRoute com nextHop como o firewall especificado que pode ser adicionado a um recurso do VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7a60e-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="7a60e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a60e-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="7a60e-111">O comando acima criará um objeto VHubRoute com nextHop como o hubVnetConnection especificado que pode então ser adicionado a um recurso VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7a60e-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="7a60e-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a60e-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="7a60e-113">Os comandos acima receberão a RoutingConfiguration de um AzVHubRoute já existente e, em seguida, adicionarão uma rota estática na conexão.</span><span class="sxs-lookup"><span data-stu-id="7a60e-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="7a60e-114">Como alternativa, se você espera criar uma nova conexão com a rota estática dentro dela, consulte o exemplo 1 [aqui.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a60e-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="7a60e-115">OS</span><span class="sxs-lookup"><span data-stu-id="7a60e-115">PARAMETERS</span></span>

### <span data-ttu-id="7a60e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a60e-116">-DefaultProfile</span></span>
<span data-ttu-id="7a60e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a60e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a60e-118">-Destino</span><span class="sxs-lookup"><span data-stu-id="7a60e-118">-Destination</span></span>
<span data-ttu-id="7a60e-119">Lista de destinos.</span><span class="sxs-lookup"><span data-stu-id="7a60e-119">List of Destinations.</span></span>

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

### <span data-ttu-id="7a60e-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="7a60e-120">-DestinationType</span></span>
<span data-ttu-id="7a60e-121">Tipo de destinos.</span><span class="sxs-lookup"><span data-stu-id="7a60e-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="7a60e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a60e-122">-Name</span></span>
<span data-ttu-id="7a60e-123">O nome da rota.</span><span class="sxs-lookup"><span data-stu-id="7a60e-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a60e-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="7a60e-124">-NextHop</span></span>
<span data-ttu-id="7a60e-125">O próximo nó.</span><span class="sxs-lookup"><span data-stu-id="7a60e-125">The next hop.</span></span>

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

### <span data-ttu-id="7a60e-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="7a60e-126">-NextHopType</span></span>
<span data-ttu-id="7a60e-127">O próximo tipo de salto.</span><span class="sxs-lookup"><span data-stu-id="7a60e-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="7a60e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a60e-128">CommonParameters</span></span>
<span data-ttu-id="7a60e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a60e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a60e-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a60e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a60e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a60e-131">INPUTS</span></span>

### <span data-ttu-id="7a60e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7a60e-132">System.String</span></span>

## <span data-ttu-id="7a60e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a60e-133">OUTPUTS</span></span>

### <span data-ttu-id="7a60e-134">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="7a60e-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="7a60e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a60e-135">NOTES</span></span>

## <span data-ttu-id="7a60e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a60e-136">RELATED LINKS</span></span>

[<span data-ttu-id="7a60e-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a60e-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="7a60e-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a60e-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="7a60e-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a60e-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="7a60e-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a60e-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)