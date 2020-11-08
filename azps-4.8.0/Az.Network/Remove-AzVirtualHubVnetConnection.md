---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111529"
---
# <span data-ttu-id="b191e-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b191e-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="b191e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b191e-102">SYNOPSIS</span></span>
<span data-ttu-id="b191e-103">O cmdlet Remove-AzVirtualHubVnetConnection remove uma conexão de rede virtual do Azure que seja uma VNET remota para a VNET do Hub.</span><span class="sxs-lookup"><span data-stu-id="b191e-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b191e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b191e-104">SYNTAX</span></span>

### <span data-ttu-id="b191e-105">ByHubVirtualNetworkConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b191e-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b191e-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b191e-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b191e-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b191e-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b191e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b191e-108">DESCRIPTION</span></span>
<span data-ttu-id="b191e-109">O cmdlet Remove-AzVirtualHubVnetConnection remove uma conexão de rede virtual do Azure que seja uma VNET remota para a VNET do Hub.</span><span class="sxs-lookup"><span data-stu-id="b191e-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b191e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b191e-110">EXAMPLES</span></span>

### <span data-ttu-id="b191e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b191e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="b191e-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b191e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b191e-113">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b191e-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b191e-114">Após a criação da conexão de rede virtual do Hub, ele remove a conexão de rede virtual do Hub usando o nome do grupo de recursos, o nome do Hub e o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="b191e-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="b191e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b191e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="b191e-116">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro dos EUA nesse grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b191e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b191e-117">Uma conexão de rede virtual será criada posteriormente, o que fará a correspondência entre a rede virtual e o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b191e-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b191e-118">Após a criação da conexão de rede virtual do Hub, ele remove a conexão de rede virtual do Hub usando o pipe do PowerShell na saída de Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="b191e-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b191e-119">OS</span><span class="sxs-lookup"><span data-stu-id="b191e-119">PARAMETERS</span></span>

### <span data-ttu-id="b191e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b191e-120">-AsJob</span></span>
<span data-ttu-id="b191e-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b191e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b191e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b191e-122">-DefaultProfile</span></span>
<span data-ttu-id="b191e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b191e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b191e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b191e-124">-Force</span></span>
<span data-ttu-id="b191e-125">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b191e-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b191e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b191e-126">-InputObject</span></span>
<span data-ttu-id="b191e-127">O recurso hubvirtualnetworkconnection a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="b191e-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b191e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b191e-128">-Name</span></span>
<span data-ttu-id="b191e-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b191e-129">The resource name.</span></span>

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

### <span data-ttu-id="b191e-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b191e-130">-ParentResourceName</span></span>
<span data-ttu-id="b191e-131">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b191e-131">The parent resource name.</span></span>

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

### <span data-ttu-id="b191e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b191e-132">-PassThru</span></span>
<span data-ttu-id="b191e-133">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b191e-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b191e-134">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b191e-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b191e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b191e-135">-ResourceGroupName</span></span>
<span data-ttu-id="b191e-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b191e-136">The resource group name.</span></span>

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

### <span data-ttu-id="b191e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b191e-137">-ResourceId</span></span>
<span data-ttu-id="b191e-138">A ID do recurso do recurso hubvirtualnetworkconnection a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="b191e-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b191e-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b191e-139">-Confirm</span></span>
<span data-ttu-id="b191e-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b191e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b191e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b191e-141">-WhatIf</span></span>
<span data-ttu-id="b191e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b191e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b191e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b191e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b191e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b191e-144">CommonParameters</span></span>
<span data-ttu-id="b191e-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b191e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b191e-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b191e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b191e-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b191e-147">INPUTS</span></span>

### <span data-ttu-id="b191e-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="b191e-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="b191e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b191e-149">System.String</span></span>

## <span data-ttu-id="b191e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b191e-150">OUTPUTS</span></span>

### <span data-ttu-id="b191e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b191e-151">System.Boolean</span></span>

## <span data-ttu-id="b191e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b191e-152">NOTES</span></span>

## <span data-ttu-id="b191e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b191e-153">RELATED LINKS</span></span>

[<span data-ttu-id="b191e-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b191e-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="b191e-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b191e-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
