---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943237"
---
# <span data-ttu-id="951e5-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="951e5-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="951e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="951e5-102">SYNOPSIS</span></span>
<span data-ttu-id="951e5-103">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="951e5-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="951e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="951e5-104">SYNTAX</span></span>

### <span data-ttu-id="951e5-105">ByVirtualHubNameByRemoteVirtualNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="951e5-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951e5-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="951e5-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951e5-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="951e5-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951e5-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="951e5-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="951e5-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="951e5-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951e5-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="951e5-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="951e5-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="951e5-111">DESCRIPTION</span></span>
<span data-ttu-id="951e5-112">O cmdlet New-AzVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="951e5-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="951e5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="951e5-113">EXAMPLES</span></span>

### <span data-ttu-id="951e5-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="951e5-114">Example 1</span></span>

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
```

<span data-ttu-id="951e5-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="951e5-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="951e5-116">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="951e5-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="951e5-117">OS</span><span class="sxs-lookup"><span data-stu-id="951e5-117">PARAMETERS</span></span>

### <span data-ttu-id="951e5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="951e5-118">-AsJob</span></span>
<span data-ttu-id="951e5-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="951e5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="951e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951e5-120">-DefaultProfile</span></span>
<span data-ttu-id="951e5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="951e5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="951e5-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="951e5-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="951e5-123">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="951e5-123">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="951e5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="951e5-124">-Name</span></span>
<span data-ttu-id="951e5-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="951e5-125">The resource name.</span></span>

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

### <span data-ttu-id="951e5-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="951e5-126">-ParentObject</span></span>
<span data-ttu-id="951e5-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="951e5-127">The parent resource.</span></span>

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

### <span data-ttu-id="951e5-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="951e5-128">-ParentResourceId</span></span>
<span data-ttu-id="951e5-129">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="951e5-129">The parent resource.</span></span>

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

### <span data-ttu-id="951e5-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="951e5-130">-ParentResourceName</span></span>
<span data-ttu-id="951e5-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="951e5-131">The resource group name.</span></span>

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

### <span data-ttu-id="951e5-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="951e5-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="951e5-133">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="951e5-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="951e5-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="951e5-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="951e5-135">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="951e5-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="951e5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951e5-136">-ResourceGroupName</span></span>
<span data-ttu-id="951e5-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="951e5-137">The resource group name.</span></span>

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

### <span data-ttu-id="951e5-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="951e5-138">-Confirm</span></span>
<span data-ttu-id="951e5-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="951e5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951e5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951e5-140">-WhatIf</span></span>
<span data-ttu-id="951e5-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="951e5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="951e5-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="951e5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951e5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951e5-143">CommonParameters</span></span>
<span data-ttu-id="951e5-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951e5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951e5-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="951e5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951e5-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="951e5-146">INPUTS</span></span>

### <span data-ttu-id="951e5-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="951e5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="951e5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="951e5-148">System.String</span></span>

## <span data-ttu-id="951e5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="951e5-149">OUTPUTS</span></span>

### <span data-ttu-id="951e5-150">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="951e5-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="951e5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="951e5-151">NOTES</span></span>

## <span data-ttu-id="951e5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="951e5-152">RELATED LINKS</span></span>

[<span data-ttu-id="951e5-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="951e5-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="951e5-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="951e5-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
