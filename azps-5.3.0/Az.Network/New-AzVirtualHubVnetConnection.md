---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429552"
---
# <span data-ttu-id="4d06e-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4d06e-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4d06e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d06e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d06e-103">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06e-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4d06e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d06e-104">SYNTAX</span></span>

### <span data-ttu-id="4d06e-105">ByVirtualHubNameByRemoteVirtualNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d06e-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d06e-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4d06e-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d06e-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4d06e-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d06e-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4d06e-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d06e-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4d06e-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d06e-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4d06e-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d06e-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d06e-111">DESCRIPTION</span></span>
<span data-ttu-id="4d06e-112">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06e-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4d06e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d06e-113">EXAMPLES</span></span>

### <span data-ttu-id="4d06e-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d06e-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
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

<span data-ttu-id="4d06e-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06e-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4d06e-116">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4d06e-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="4d06e-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4d06e-117">Example 2</span></span>

<span data-ttu-id="4d06e-118">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06e-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="4d06e-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="4d06e-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="4d06e-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4d06e-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

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
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="4d06e-121">A seguir, você criará uma nova configuração de roteamento e criará rotas estáticas na configuração de roteamento com o próximo nó como um endereço IP especificado.</span><span class="sxs-lookup"><span data-stu-id="4d06e-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="4d06e-122">Essa configuração de roteamento pode então ser passada para o comando New-AzVirtualHubVnetConnection como o parâmetro-RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d06e-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="4d06e-123">OS</span><span class="sxs-lookup"><span data-stu-id="4d06e-123">PARAMETERS</span></span>

### <span data-ttu-id="4d06e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d06e-124">-AsJob</span></span>
<span data-ttu-id="4d06e-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4d06e-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d06e-126">-DefaultProfile</span></span>
<span data-ttu-id="4d06e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d06e-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="4d06e-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="4d06e-129">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="4d06e-129">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="4d06e-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="4d06e-131">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="4d06e-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d06e-132">-Name</span></span>
<span data-ttu-id="4d06e-133">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d06e-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d06e-134">-ParentObject</span></span>
<span data-ttu-id="4d06e-135">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4d06e-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4d06e-136">-ParentResourceId</span></span>
<span data-ttu-id="4d06e-137">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4d06e-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4d06e-138">-ParentResourceName</span></span>
<span data-ttu-id="4d06e-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d06e-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4d06e-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="4d06e-141">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4d06e-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4d06e-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="4d06e-143">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4d06e-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d06e-144">-ResourceGroupName</span></span>
<span data-ttu-id="4d06e-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d06e-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06e-146">-RoutingConfiguration</span></span>
<span data-ttu-id="4d06e-147">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="4d06e-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d06e-148">-Confirm</span></span>
<span data-ttu-id="4d06e-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d06e-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d06e-150">-WhatIf</span></span>
<span data-ttu-id="4d06e-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d06e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d06e-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d06e-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d06e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d06e-153">CommonParameters</span></span>
<span data-ttu-id="4d06e-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d06e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d06e-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d06e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d06e-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d06e-156">INPUTS</span></span>

### <span data-ttu-id="4d06e-157">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4d06e-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4d06e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4d06e-158">System.String</span></span>

## <span data-ttu-id="4d06e-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d06e-159">OUTPUTS</span></span>

### <span data-ttu-id="4d06e-160">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4d06e-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4d06e-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d06e-161">NOTES</span></span>

## <span data-ttu-id="4d06e-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d06e-162">RELATED LINKS</span></span>

[<span data-ttu-id="4d06e-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4d06e-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4d06e-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4d06e-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4d06e-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d06e-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
