---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114361"
---
# <span data-ttu-id="3e657-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3e657-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3e657-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e657-102">SYNOPSIS</span></span>
<span data-ttu-id="3e657-103">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e657-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="3e657-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e657-104">SYNTAX</span></span>

### <span data-ttu-id="3e657-105">ByVirtualHubNameByRemoteVirtualNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e657-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e657-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3e657-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e657-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3e657-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e657-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3e657-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e657-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3e657-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e657-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3e657-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e657-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e657-111">DESCRIPTION</span></span>
<span data-ttu-id="3e657-112">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e657-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="3e657-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e657-113">EXAMPLES</span></span>

### <span data-ttu-id="3e657-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e657-114">Example 1</span></span>

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

<span data-ttu-id="3e657-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e657-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3e657-116">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="3e657-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="3e657-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e657-117">Example 2</span></span>

<span data-ttu-id="3e657-118">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e657-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="3e657-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="3e657-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="3e657-120">OS</span><span class="sxs-lookup"><span data-stu-id="3e657-120">PARAMETERS</span></span>

### <span data-ttu-id="3e657-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e657-121">-AsJob</span></span>
<span data-ttu-id="3e657-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3e657-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e657-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e657-123">-DefaultProfile</span></span>
<span data-ttu-id="3e657-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e657-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e657-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="3e657-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="3e657-126">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="3e657-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="3e657-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="3e657-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="3e657-128">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="3e657-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="3e657-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e657-129">-Name</span></span>
<span data-ttu-id="3e657-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e657-130">The resource name.</span></span>

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

### <span data-ttu-id="3e657-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3e657-131">-ParentObject</span></span>
<span data-ttu-id="3e657-132">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="3e657-132">The parent resource.</span></span>

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

### <span data-ttu-id="3e657-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3e657-133">-ParentResourceId</span></span>
<span data-ttu-id="3e657-134">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="3e657-134">The parent resource.</span></span>

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

### <span data-ttu-id="3e657-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3e657-135">-ParentResourceName</span></span>
<span data-ttu-id="3e657-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e657-136">The resource group name.</span></span>

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

### <span data-ttu-id="3e657-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e657-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="3e657-138">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="3e657-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="3e657-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3e657-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="3e657-140">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="3e657-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="3e657-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e657-141">-ResourceGroupName</span></span>
<span data-ttu-id="3e657-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e657-142">The resource group name.</span></span>

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

### <span data-ttu-id="3e657-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e657-143">-RoutingConfiguration</span></span>
<span data-ttu-id="3e657-144">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="3e657-144">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="3e657-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e657-145">-Confirm</span></span>
<span data-ttu-id="3e657-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e657-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e657-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e657-147">-WhatIf</span></span>
<span data-ttu-id="3e657-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e657-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e657-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e657-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e657-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e657-150">CommonParameters</span></span>
<span data-ttu-id="3e657-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e657-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e657-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e657-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e657-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e657-153">INPUTS</span></span>

### <span data-ttu-id="3e657-154">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3e657-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3e657-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3e657-155">System.String</span></span>

## <span data-ttu-id="3e657-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e657-156">OUTPUTS</span></span>

### <span data-ttu-id="3e657-157">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3e657-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3e657-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e657-158">NOTES</span></span>

## <span data-ttu-id="3e657-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e657-159">RELATED LINKS</span></span>

[<span data-ttu-id="3e657-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3e657-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="3e657-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3e657-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="3e657-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e657-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
