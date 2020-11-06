---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: b4b0253814c6488c5f7269c6a79d51790a2f39fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600170"
---
# <span data-ttu-id="71099-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="71099-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="71099-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71099-102">SYNOPSIS</span></span>
<span data-ttu-id="71099-103">O cmdlet Remove-AzExpressRouteGateway remove um gateway do Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71099-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="71099-104">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="71099-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="71099-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71099-105">SYNTAX</span></span>

### <span data-ttu-id="71099-106">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="71099-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71099-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="71099-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71099-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="71099-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71099-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71099-109">DESCRIPTION</span></span>
<span data-ttu-id="71099-110">O cmdlet Remove-AzExpressRouteGateway remove um gateway do Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71099-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="71099-111">Esse é um gateway específico para a conectividade definida pelo software da WAN virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="71099-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="71099-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71099-112">EXAMPLES</span></span>

### <span data-ttu-id="71099-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71099-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="71099-114">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway do ExpressRoute escalável no centro dos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="71099-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="71099-115">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="71099-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="71099-116">Isso excluirá o ExpressRouteGateway e todos os ExpressRouteConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="71099-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="71099-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="71099-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="71099-118">Este exemplo cria um grupo de recursos, uma WAN virtual, um hub virtual, um gateway de ExpressRoute escalável no centro oeste dos EUA e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="71099-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="71099-119">Essa exclusão ocorre usando o pipe do PowerShell, que usa o objeto ExpressRouteGateway retornado pelo comando Get-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="71099-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="71099-120">Para suprimir o prompt ao excluir o gateway virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="71099-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="71099-121">Isso excluirá o ExpressRouteGateway e todos os ExpressRouteConnections anexados a ele.</span><span class="sxs-lookup"><span data-stu-id="71099-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="71099-122">OS</span><span class="sxs-lookup"><span data-stu-id="71099-122">PARAMETERS</span></span>

### <span data-ttu-id="71099-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71099-123">-DefaultProfile</span></span>
<span data-ttu-id="71099-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71099-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71099-125">-Force</span><span class="sxs-lookup"><span data-stu-id="71099-125">-Force</span></span>
<span data-ttu-id="71099-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="71099-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="71099-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71099-127">-InputObject</span></span>
<span data-ttu-id="71099-128">O objeto ExpressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="71099-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="71099-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="71099-129">-Name</span></span>
<span data-ttu-id="71099-130">O nome ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="71099-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="71099-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71099-131">-PassThru</span></span>
<span data-ttu-id="71099-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="71099-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71099-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="71099-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71099-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71099-134">-ResourceGroupName</span></span>
<span data-ttu-id="71099-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71099-135">The resource group name.</span></span>

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

### <span data-ttu-id="71099-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71099-136">-ResourceId</span></span>
<span data-ttu-id="71099-137">A ID de recurso do Azure para o ExpressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="71099-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="71099-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71099-138">-Confirm</span></span>
<span data-ttu-id="71099-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71099-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71099-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71099-140">-WhatIf</span></span>
<span data-ttu-id="71099-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71099-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71099-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71099-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71099-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71099-143">CommonParameters</span></span>
<span data-ttu-id="71099-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71099-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71099-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71099-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71099-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71099-146">INPUTS</span></span>

### <span data-ttu-id="71099-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="71099-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="71099-148">System. String</span><span class="sxs-lookup"><span data-stu-id="71099-148">System.String</span></span>

## <span data-ttu-id="71099-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71099-149">OUTPUTS</span></span>

### <span data-ttu-id="71099-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71099-150">System.Boolean</span></span>

## <span data-ttu-id="71099-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71099-151">NOTES</span></span>

## <span data-ttu-id="71099-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71099-152">RELATED LINKS</span></span>
