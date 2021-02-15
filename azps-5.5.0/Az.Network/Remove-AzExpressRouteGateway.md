---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111589"
---
# <span data-ttu-id="279f2-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="279f2-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="279f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="279f2-102">SYNOPSIS</span></span>
<span data-ttu-id="279f2-103">O Remove-AzExpressRouteGateway cmdlet remove um gateway do Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="279f2-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="279f2-104">Este é um gateway específico para a conectividade definida pelo software WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="279f2-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="279f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="279f2-105">SYNTAX</span></span>

### <span data-ttu-id="279f2-106">ByExpressRouteGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="279f2-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279f2-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="279f2-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279f2-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="279f2-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279f2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="279f2-109">DESCRIPTION</span></span>
<span data-ttu-id="279f2-110">O Remove-AzExpressRouteGateway cmdlet remove um gateway do Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="279f2-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="279f2-111">Este é um gateway específico para a conectividade definida pelo software WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="279f2-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="279f2-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="279f2-112">EXAMPLES</span></span>

### <span data-ttu-id="279f2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="279f2-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="279f2-114">Este exemplo cria um grupo De recursos, WAN Virtual, Hub Virtual, gateway escalável do ExpressRoute na Central dos EUA e o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="279f2-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="279f2-115">Para suprimir o prompt ao excluir o Gateway Virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="279f2-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="279f2-116">Isso excluirá o ExpressRouteGateway e todas as ExpressRouteConnections anexadas a ele.</span><span class="sxs-lookup"><span data-stu-id="279f2-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="279f2-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="279f2-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="279f2-118">Este exemplo cria um grupo De recursos, WAN Virtual, Hub Virtual, gateway escalonável do ExpressRoute no Centro Oeste dos EUA e o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="279f2-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="279f2-119">Essa exclusão acontece usando a piping do PowerShell, que usa o objeto ExpressRouteGateway retornado pelo comando Get-AzExpressRouteGateway comando.</span><span class="sxs-lookup"><span data-stu-id="279f2-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="279f2-120">Para suprimir o prompt ao excluir o Gateway Virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="279f2-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="279f2-121">Isso excluirá o ExpressRouteGateway e todas as ExpressRouteConnections anexadas a ele.</span><span class="sxs-lookup"><span data-stu-id="279f2-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="279f2-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="279f2-122">PARAMETERS</span></span>

### <span data-ttu-id="279f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279f2-123">-DefaultProfile</span></span>
<span data-ttu-id="279f2-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="279f2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279f2-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="279f2-125">-Force</span></span>
<span data-ttu-id="279f2-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="279f2-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="279f2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279f2-127">-InputObject</span></span>
<span data-ttu-id="279f2-128">O objeto ExpressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="279f2-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="279f2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="279f2-129">-Name</span></span>
<span data-ttu-id="279f2-130">O nome do ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="279f2-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279f2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279f2-131">-PassThru</span></span>
<span data-ttu-id="279f2-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="279f2-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="279f2-133">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="279f2-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="279f2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279f2-134">-ResourceGroupName</span></span>
<span data-ttu-id="279f2-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="279f2-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279f2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279f2-136">-ResourceId</span></span>
<span data-ttu-id="279f2-137">A ID de recurso do Azure para que o ExpressRouteGateway seja excluído.</span><span class="sxs-lookup"><span data-stu-id="279f2-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279f2-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="279f2-138">-Confirm</span></span>
<span data-ttu-id="279f2-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="279f2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279f2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279f2-140">-WhatIf</span></span>
<span data-ttu-id="279f2-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="279f2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279f2-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="279f2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279f2-143">CommonParameters</span></span>
<span data-ttu-id="279f2-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279f2-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="279f2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279f2-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="279f2-146">INPUTS</span></span>

### <span data-ttu-id="279f2-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="279f2-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="279f2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="279f2-148">System.String</span></span>

## <span data-ttu-id="279f2-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="279f2-149">OUTPUTS</span></span>

### <span data-ttu-id="279f2-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="279f2-150">System.Boolean</span></span>

## <span data-ttu-id="279f2-151">Notas</span><span class="sxs-lookup"><span data-stu-id="279f2-151">NOTES</span></span>

## <span data-ttu-id="279f2-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="279f2-152">RELATED LINKS</span></span>
