---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886884"
---
# <span data-ttu-id="28334-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="28334-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="28334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28334-102">SYNOPSIS</span></span>
<span data-ttu-id="28334-103">Atualiza um Gateway ExpressRoute Escalonável.</span><span class="sxs-lookup"><span data-stu-id="28334-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="28334-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28334-104">SYNTAX</span></span>

### <span data-ttu-id="28334-105">ByExpressRouteGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28334-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28334-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="28334-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28334-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="28334-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28334-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28334-108">DESCRIPTION</span></span>

<span data-ttu-id="28334-109">O cmdlet **Set-AzExpressRouteGateway** permite que você atualize as unidades de escala para um ExpressRouteGateway existente ou atualize as marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="28334-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="28334-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28334-110">EXAMPLES</span></span>

### <span data-ttu-id="28334-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28334-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="28334-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="28334-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="28334-113">Um gateway ExpressRoute será criado posteriormente no Hub Virtual com 2 unidades de escala que serão modificadas para 3 unidades de escala</span><span class="sxs-lookup"><span data-stu-id="28334-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="28334-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28334-114">PARAMETERS</span></span>

### <span data-ttu-id="28334-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28334-115">-AsJob</span></span>
<span data-ttu-id="28334-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28334-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28334-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28334-117">-DefaultProfile</span></span>
<span data-ttu-id="28334-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28334-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28334-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28334-119">-InputObject</span></span>
<span data-ttu-id="28334-120">O ExpressRouteGateway que precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="28334-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="28334-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="28334-121">-MaxScaleUnits</span></span>
<span data-ttu-id="28334-122">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="28334-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="28334-123">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="28334-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28334-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="28334-124">-MinScaleUnits</span></span>
<span data-ttu-id="28334-125">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="28334-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="28334-126">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="28334-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28334-127">-Name</span><span class="sxs-lookup"><span data-stu-id="28334-127">-Name</span></span>
<span data-ttu-id="28334-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="28334-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28334-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28334-129">-ResourceGroupName</span></span>
<span data-ttu-id="28334-130">O nome do grupo de recursos do ExpressRouteGateway a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="28334-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="28334-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28334-131">-ResourceId</span></span>
<span data-ttu-id="28334-132">A ID do ExpressRouteGateway que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="28334-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28334-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="28334-133">-Tag</span></span>
<span data-ttu-id="28334-134">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="28334-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28334-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28334-135">-Confirm</span></span>
<span data-ttu-id="28334-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28334-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28334-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28334-137">-WhatIf</span></span>
<span data-ttu-id="28334-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28334-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28334-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28334-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28334-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28334-140">CommonParameters</span></span>
<span data-ttu-id="28334-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28334-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28334-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28334-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28334-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28334-143">INPUTS</span></span>

### <span data-ttu-id="28334-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="28334-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="28334-145">System.String</span><span class="sxs-lookup"><span data-stu-id="28334-145">System.String</span></span>

## <span data-ttu-id="28334-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28334-146">OUTPUTS</span></span>

### <span data-ttu-id="28334-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="28334-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="28334-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="28334-148">NOTES</span></span>

## <span data-ttu-id="28334-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28334-149">RELATED LINKS</span></span>
