---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778451"
---
# <span data-ttu-id="5cbec-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5cbec-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="5cbec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cbec-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbec-103">Atualiza um HubVirtualNetworkConnection existente.</span><span class="sxs-lookup"><span data-stu-id="5cbec-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="5cbec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cbec-104">SYNTAX</span></span>

### <span data-ttu-id="5cbec-105">ByHubVirtualNetworkConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5cbec-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cbec-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5cbec-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cbec-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="5cbec-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cbec-108">DESCRIPTION</span></span>
<span data-ttu-id="5cbec-109">Atualiza um HubVirtualNetworkConnection existente.</span><span class="sxs-lookup"><span data-stu-id="5cbec-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="5cbec-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cbec-110">EXAMPLES</span></span>

### <span data-ttu-id="5cbec-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5cbec-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="5cbec-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbec-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="5cbec-113">Uma conexão de rede virtual também é criada, o que é par da rede virtual ao Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="5cbec-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="5cbec-114">Esta conexão de rede virtual é atualizada para habilitar a segurança da Internet.</span><span class="sxs-lookup"><span data-stu-id="5cbec-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="5cbec-115">OS</span><span class="sxs-lookup"><span data-stu-id="5cbec-115">PARAMETERS</span></span>

### <span data-ttu-id="5cbec-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cbec-116">-AsJob</span></span>
<span data-ttu-id="5cbec-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5cbec-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cbec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbec-118">-DefaultProfile</span></span>
<span data-ttu-id="5cbec-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5cbec-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="5cbec-121">Habilite a segurança da Internet para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="5cbec-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cbec-122">-InputObject</span></span>
<span data-ttu-id="5cbec-123">O recurso hubvirtualnetworkconnection a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="5cbec-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cbec-124">-Name</span></span>
<span data-ttu-id="5cbec-125">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5cbec-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5cbec-126">-ParentResourceName</span></span>
<span data-ttu-id="5cbec-127">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="5cbec-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbec-128">-ResourceGroupName</span></span>
<span data-ttu-id="5cbec-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cbec-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cbec-130">-ResourceId</span></span>
<span data-ttu-id="5cbec-131">A ID do recurso do recurso hubvirtualnetworkconnection a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="5cbec-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cbec-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5cbec-132">-Confirm</span></span>
<span data-ttu-id="5cbec-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbec-134">-WhatIf</span></span>
<span data-ttu-id="5cbec-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cbec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbec-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cbec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbec-137">CommonParameters</span></span>
<span data-ttu-id="5cbec-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbec-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbec-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbec-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cbec-140">INPUTS</span></span>

### <span data-ttu-id="5cbec-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5cbec-141">System.String</span></span>

### <span data-ttu-id="5cbec-142">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="5cbec-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="5cbec-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cbec-143">OUTPUTS</span></span>

### <span data-ttu-id="5cbec-144">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="5cbec-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="5cbec-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cbec-145">NOTES</span></span>

## <span data-ttu-id="5cbec-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cbec-146">RELATED LINKS</span></span>