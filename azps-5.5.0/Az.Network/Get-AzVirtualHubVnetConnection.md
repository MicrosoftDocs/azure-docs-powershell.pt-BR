---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 688168317a622cb0375bb111050f3e54696047ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111683"
---
# <span data-ttu-id="6580c-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6580c-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="6580c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6580c-102">SYNOPSIS</span></span>
<span data-ttu-id="6580c-103">Obtém uma Conexão de Rede Virtual em um hub virtual ou lista todas as conexões de rede virtuais em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="6580c-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="6580c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6580c-104">SYNTAX</span></span>

### <span data-ttu-id="6580c-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6580c-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6580c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6580c-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6580c-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6580c-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6580c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6580c-108">DESCRIPTION</span></span>
<span data-ttu-id="6580c-109">Obtém uma Conexão de Rede Virtual em um hub virtual ou lista todas as conexões de rede virtuais em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="6580c-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="6580c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6580c-110">EXAMPLES</span></span>

### <span data-ttu-id="6580c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6580c-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="6580c-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual na Central dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="6580c-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="6580c-113">Uma Conexão de Rede Virtual será criada a partir daí, que irá fazer a conexão da Rede Virtual com o Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="6580c-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="6580c-114">Depois que a conexão de rede virtual do hub é criada, ela obtém a conexão de rede virtual do hub usando o nome do grupo de recursos, o nome do hub e o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="6580c-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="6580c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6580c-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="6580c-116">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual na Central dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="6580c-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="6580c-117">Uma Conexão de Rede Virtual será criada a partir daí, que irá fazer o mesmo com a Rede Virtual com o Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="6580c-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="6580c-118">Depois que a conexão de rede virtual do hub é criada, ela lista toda a conexão de rede virtual do hub usando o nome do grupo de recursos e o nome do hub.</span><span class="sxs-lookup"><span data-stu-id="6580c-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="6580c-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6580c-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="6580c-120">Este cmdlet lista todas as conexões de rede virtual do hub começando com "teste" usando o nome do grupo de recursos e o nome do hub.</span><span class="sxs-lookup"><span data-stu-id="6580c-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="6580c-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6580c-121">PARAMETERS</span></span>

### <span data-ttu-id="6580c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6580c-122">-DefaultProfile</span></span>
<span data-ttu-id="6580c-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6580c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6580c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6580c-124">-Name</span></span>
<span data-ttu-id="6580c-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6580c-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6580c-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6580c-126">-ParentObject</span></span>
<span data-ttu-id="6580c-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="6580c-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6580c-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6580c-128">-ParentResourceId</span></span>
<span data-ttu-id="6580c-129">A ID do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="6580c-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6580c-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6580c-130">-ParentResourceName</span></span>
<span data-ttu-id="6580c-131">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="6580c-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6580c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6580c-132">-ResourceGroupName</span></span>
<span data-ttu-id="6580c-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6580c-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6580c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6580c-134">CommonParameters</span></span>
<span data-ttu-id="6580c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6580c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6580c-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6580c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6580c-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="6580c-137">INPUTS</span></span>

### <span data-ttu-id="6580c-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6580c-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6580c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6580c-139">System.String</span></span>

## <span data-ttu-id="6580c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="6580c-140">OUTPUTS</span></span>

### <span data-ttu-id="6580c-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="6580c-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="6580c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="6580c-142">NOTES</span></span>

## <span data-ttu-id="6580c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6580c-143">RELATED LINKS</span></span>

[<span data-ttu-id="6580c-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6580c-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="6580c-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6580c-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
