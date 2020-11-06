---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 87591f5ecf928fb2dc9444fd826ce03f484e665c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600087"
---
# <span data-ttu-id="940d1-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="940d1-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="940d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="940d1-102">SYNOPSIS</span></span>
<span data-ttu-id="940d1-103">Remove um VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="940d1-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="940d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="940d1-104">SYNTAX</span></span>

### <span data-ttu-id="940d1-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="940d1-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940d1-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="940d1-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940d1-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="940d1-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="940d1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="940d1-108">DESCRIPTION</span></span>
<span data-ttu-id="940d1-109">Remove um VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="940d1-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="940d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="940d1-110">EXAMPLES</span></span>

### <span data-ttu-id="940d1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="940d1-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="940d1-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="940d1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="940d1-113">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="940d1-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="940d1-114">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="940d1-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="940d1-115">Em seguida, ele remove a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="940d1-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="940d1-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="940d1-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="940d1-117">Mesmo que o exemplo 1, mas agora ele remove a conexão usando o objeto piped do Get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="940d1-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="940d1-118">OS</span><span class="sxs-lookup"><span data-stu-id="940d1-118">PARAMETERS</span></span>

### <span data-ttu-id="940d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940d1-119">-DefaultProfile</span></span>
<span data-ttu-id="940d1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="940d1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="940d1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="940d1-121">-Force</span></span>
<span data-ttu-id="940d1-122">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="940d1-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="940d1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="940d1-123">-InputObject</span></span>
<span data-ttu-id="940d1-124">O objeto VpnConenction a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="940d1-124">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="940d1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="940d1-125">-Name</span></span>
<span data-ttu-id="940d1-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="940d1-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d1-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="940d1-127">-ParentResourceName</span></span>
<span data-ttu-id="940d1-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="940d1-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="940d1-129">-PassThru</span></span>
<span data-ttu-id="940d1-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="940d1-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="940d1-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="940d1-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="940d1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940d1-132">-ResourceGroupName</span></span>
<span data-ttu-id="940d1-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="940d1-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940d1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940d1-134">-ResourceId</span></span>
<span data-ttu-id="940d1-135">A ID do recurso do objeto VpnConenction a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="940d1-135">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="940d1-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="940d1-136">-Confirm</span></span>
<span data-ttu-id="940d1-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="940d1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940d1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940d1-138">-WhatIf</span></span>
<span data-ttu-id="940d1-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="940d1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940d1-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="940d1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940d1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940d1-141">CommonParameters</span></span>
<span data-ttu-id="940d1-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940d1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940d1-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940d1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940d1-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="940d1-144">INPUTS</span></span>

### <span data-ttu-id="940d1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="940d1-145">System.String</span></span>

### <span data-ttu-id="940d1-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="940d1-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="940d1-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="940d1-147">OUTPUTS</span></span>

### <span data-ttu-id="940d1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="940d1-148">System.Boolean</span></span>

## <span data-ttu-id="940d1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="940d1-149">NOTES</span></span>

## <span data-ttu-id="940d1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="940d1-150">RELATED LINKS</span></span>

[<span data-ttu-id="940d1-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="940d1-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="940d1-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="940d1-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="940d1-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="940d1-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
