---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440327"
---
# <span data-ttu-id="cd854-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cd854-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="cd854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd854-102">SYNOPSIS</span></span>
<span data-ttu-id="cd854-103">O cmdlet Remove-AzureRmVpnGateway remove um gateway de VPN do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd854-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="cd854-104">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="cd854-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd854-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd854-105">SYNTAX</span></span>

### <span data-ttu-id="cd854-106">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd854-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd854-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cd854-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd854-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cd854-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd854-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd854-109">DESCRIPTION</span></span>
<span data-ttu-id="cd854-110">O cmdlet Remove-AzureRmVpnGateway remove um gateway de VPN do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd854-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="cd854-111">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="cd854-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="cd854-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd854-112">EXAMPLES</span></span>

### <span data-ttu-id="cd854-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd854-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="cd854-114">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway VPN escalável nos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cd854-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="cd854-115">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="cd854-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="cd854-116">Isso excluirá o VpnGateway e todos os VpnConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="cd854-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="cd854-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd854-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="cd854-118">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway VPN escalável nos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cd854-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="cd854-119">Essa exclusão ocorre usando o pipe do PowerShell, que usa o objeto VpnGateway retornado pelo comando Get-AzureRmVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cd854-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="cd854-120">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="cd854-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="cd854-121">Isso excluirá o VpnGateway e todos os VpnConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="cd854-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="cd854-122">OS</span><span class="sxs-lookup"><span data-stu-id="cd854-122">PARAMETERS</span></span>

### <span data-ttu-id="cd854-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd854-123">-DefaultProfile</span></span>
<span data-ttu-id="cd854-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd854-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd854-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cd854-125">-Force</span></span>
<span data-ttu-id="cd854-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="cd854-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cd854-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd854-127">-InputObject</span></span>
<span data-ttu-id="cd854-128">O objeto vpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cd854-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="cd854-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd854-129">-Name</span></span>
<span data-ttu-id="cd854-130">O nome vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cd854-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="cd854-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd854-131">-PassThru</span></span>
<span data-ttu-id="cd854-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cd854-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd854-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cd854-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd854-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd854-134">-ResourceGroupName</span></span>
<span data-ttu-id="cd854-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd854-135">The resource group name.</span></span>

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

### <span data-ttu-id="cd854-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd854-136">-ResourceId</span></span>
<span data-ttu-id="cd854-137">A ID de recurso do Azure para o vpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cd854-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="cd854-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd854-138">-Confirm</span></span>
<span data-ttu-id="cd854-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd854-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd854-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd854-140">-WhatIf</span></span>
<span data-ttu-id="cd854-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd854-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd854-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd854-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd854-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd854-143">CommonParameters</span></span>
<span data-ttu-id="cd854-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd854-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd854-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd854-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd854-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd854-146">INPUTS</span></span>

### <span data-ttu-id="cd854-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cd854-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="cd854-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cd854-148">System.String</span></span>

## <span data-ttu-id="cd854-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd854-149">OUTPUTS</span></span>

### <span data-ttu-id="cd854-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd854-150">System.Boolean</span></span>

## <span data-ttu-id="cd854-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd854-151">NOTES</span></span>

## <span data-ttu-id="cd854-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd854-152">RELATED LINKS</span></span>
