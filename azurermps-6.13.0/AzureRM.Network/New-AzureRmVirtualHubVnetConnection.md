---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603148"
---
# <span data-ttu-id="4ebad-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ebad-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4ebad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ebad-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebad-103">O cmdlet New-AzureRmVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebad-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ebad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebad-104">SYNTAX</span></span>

### <span data-ttu-id="4ebad-105">ByVirtualHubNameByRemoteVirtualNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ebad-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebad-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebad-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebad-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4ebad-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebad-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebad-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebad-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4ebad-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebad-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebad-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebad-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ebad-111">DESCRIPTION</span></span>
<span data-ttu-id="4ebad-112">O cmdlet New-AzureRmVirtualHubVnetConnection cria um recurso HubVirtualNetworkConnection que peer uma rede virtual para o Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebad-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4ebad-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ebad-113">EXAMPLES</span></span>

### <span data-ttu-id="4ebad-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ebad-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="4ebad-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebad-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4ebad-116">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4ebad-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="4ebad-117">OS</span><span class="sxs-lookup"><span data-stu-id="4ebad-117">PARAMETERS</span></span>

### <span data-ttu-id="4ebad-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ebad-118">-AsJob</span></span>
<span data-ttu-id="4ebad-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4ebad-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebad-120">-DefaultProfile</span></span>
<span data-ttu-id="4ebad-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ebad-122">-Name</span></span>
<span data-ttu-id="4ebad-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4ebad-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4ebad-124">-ParentObject</span></span>
<span data-ttu-id="4ebad-125">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4ebad-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ebad-126">-ParentResourceId</span></span>
<span data-ttu-id="4ebad-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4ebad-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4ebad-128">-ParentResourceName</span></span>
<span data-ttu-id="4ebad-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ebad-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ebad-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="4ebad-131">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4ebad-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4ebad-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="4ebad-133">A rede virtual remota à qual a conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4ebad-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebad-134">-ResourceGroupName</span></span>
<span data-ttu-id="4ebad-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ebad-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ebad-136">-Confirm</span></span>
<span data-ttu-id="4ebad-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebad-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebad-138">-WhatIf</span></span>
<span data-ttu-id="4ebad-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ebad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ebad-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ebad-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebad-141">CommonParameters</span></span>
<span data-ttu-id="4ebad-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebad-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebad-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebad-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ebad-144">INPUTS</span></span>

### <span data-ttu-id="4ebad-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4ebad-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4ebad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebad-146">System.String</span></span>

## <span data-ttu-id="4ebad-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ebad-147">OUTPUTS</span></span>

### <span data-ttu-id="4ebad-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4ebad-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4ebad-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ebad-149">NOTES</span></span>

## <span data-ttu-id="4ebad-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ebad-150">RELATED LINKS</span></span>
