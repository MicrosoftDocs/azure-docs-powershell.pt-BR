---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943943"
---
# <span data-ttu-id="e5311-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5311-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="e5311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5311-102">SYNOPSIS</span></span>
<span data-ttu-id="e5311-103">O cmdlet Remove-AzVpnGateway remove um gateway de VPN do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5311-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="e5311-104">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="e5311-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e5311-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5311-105">SYNTAX</span></span>

### <span data-ttu-id="e5311-106">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5311-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5311-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e5311-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5311-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e5311-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5311-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5311-109">DESCRIPTION</span></span>
<span data-ttu-id="e5311-110">O cmdlet Remove-AzVpnGateway remove um gateway de VPN do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5311-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="e5311-111">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="e5311-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="e5311-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5311-112">EXAMPLES</span></span>

### <span data-ttu-id="e5311-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5311-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="e5311-114">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway VPN escalável nos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e5311-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="e5311-115">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="e5311-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e5311-116">Isso excluirá o VpnGateway e todos os VpnConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="e5311-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="e5311-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e5311-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="e5311-118">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway VPN escalável nos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e5311-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="e5311-119">Essa exclusão ocorre usando o pipe do PowerShell, que usa o objeto VpnGateway retornado pelo comando Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e5311-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="e5311-120">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="e5311-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="e5311-121">Isso excluirá o VpnGateway e todos os VpnConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="e5311-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="e5311-122">OS</span><span class="sxs-lookup"><span data-stu-id="e5311-122">PARAMETERS</span></span>

### <span data-ttu-id="e5311-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5311-123">-DefaultProfile</span></span>
<span data-ttu-id="e5311-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5311-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5311-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e5311-125">-Force</span></span>
<span data-ttu-id="e5311-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e5311-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e5311-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5311-127">-InputObject</span></span>
<span data-ttu-id="e5311-128">O objeto vpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e5311-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5311-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5311-129">-Name</span></span>
<span data-ttu-id="e5311-130">O nome vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e5311-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5311-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5311-131">-PassThru</span></span>
<span data-ttu-id="e5311-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e5311-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5311-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e5311-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5311-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5311-134">-ResourceGroupName</span></span>
<span data-ttu-id="e5311-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5311-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5311-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5311-136">-ResourceId</span></span>
<span data-ttu-id="e5311-137">A ID de recurso do Azure para o vpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e5311-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5311-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5311-138">-Confirm</span></span>
<span data-ttu-id="e5311-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5311-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5311-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5311-140">-WhatIf</span></span>
<span data-ttu-id="e5311-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5311-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5311-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5311-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5311-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5311-143">CommonParameters</span></span>
<span data-ttu-id="e5311-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5311-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5311-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5311-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5311-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5311-146">INPUTS</span></span>

### <span data-ttu-id="e5311-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5311-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e5311-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e5311-148">System.String</span></span>

## <span data-ttu-id="e5311-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5311-149">OUTPUTS</span></span>

### <span data-ttu-id="e5311-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5311-150">System.Boolean</span></span>

## <span data-ttu-id="e5311-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5311-151">NOTES</span></span>

## <span data-ttu-id="e5311-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5311-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5311-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5311-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="e5311-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5311-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="e5311-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5311-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
