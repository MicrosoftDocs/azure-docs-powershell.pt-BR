---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: c3d311cc091026bcd08225e5a11a8232102a03a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772209"
---
# <span data-ttu-id="aa411-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="aa411-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="aa411-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa411-102">SYNOPSIS</span></span>
<span data-ttu-id="aa411-103">Atualiza um gateway ExpressRoute dimensionável.</span><span class="sxs-lookup"><span data-stu-id="aa411-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="aa411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa411-104">SYNTAX</span></span>

### <span data-ttu-id="aa411-105">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa411-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa411-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="aa411-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa411-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="aa411-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa411-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa411-108">DESCRIPTION</span></span>

<span data-ttu-id="aa411-109">Set-AzExpressRouteGateway atualiza as unidades de escala da ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="aa411-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="aa411-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa411-110">EXAMPLES</span></span>

### <span data-ttu-id="aa411-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa411-111">Example 1</span></span>

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

<span data-ttu-id="aa411-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa411-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="aa411-113">Um gateway do ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala que serão modificadas para 3 unidades de escala</span><span class="sxs-lookup"><span data-stu-id="aa411-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="aa411-114">OS</span><span class="sxs-lookup"><span data-stu-id="aa411-114">PARAMETERS</span></span>

### <span data-ttu-id="aa411-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa411-115">-AsJob</span></span>
<span data-ttu-id="aa411-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa411-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa411-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa411-117">-DefaultProfile</span></span>
<span data-ttu-id="aa411-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa411-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa411-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa411-119">-InputObject</span></span>
<span data-ttu-id="aa411-120">O ExpressRouteGateway que precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="aa411-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="aa411-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="aa411-121">-MaxScaleUnits</span></span>
<span data-ttu-id="aa411-122">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="aa411-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="aa411-123">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="aa411-123">Valid range > 2</span></span>

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

### <span data-ttu-id="aa411-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="aa411-124">-MinScaleUnits</span></span>
<span data-ttu-id="aa411-125">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="aa411-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="aa411-126">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="aa411-126">Valid range > 2</span></span>

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

### <span data-ttu-id="aa411-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa411-127">-Name</span></span>
<span data-ttu-id="aa411-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="aa411-128">The resource name.</span></span>

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

### <span data-ttu-id="aa411-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa411-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa411-130">O nome do grupo de recursos do ExpressRouteGateway a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="aa411-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="aa411-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa411-131">-ResourceId</span></span>
<span data-ttu-id="aa411-132">A ID do ExpressRouteGateway que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="aa411-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="aa411-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="aa411-133">-Tag</span></span>
<span data-ttu-id="aa411-134">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa411-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="aa411-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa411-135">-Confirm</span></span>
<span data-ttu-id="aa411-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa411-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa411-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa411-137">-WhatIf</span></span>
<span data-ttu-id="aa411-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa411-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa411-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa411-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa411-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa411-140">CommonParameters</span></span>
<span data-ttu-id="aa411-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa411-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa411-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa411-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa411-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa411-143">INPUTS</span></span>

### <span data-ttu-id="aa411-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="aa411-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="aa411-145">System. String</span><span class="sxs-lookup"><span data-stu-id="aa411-145">System.String</span></span>

## <span data-ttu-id="aa411-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa411-146">OUTPUTS</span></span>

### <span data-ttu-id="aa411-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="aa411-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="aa411-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa411-148">NOTES</span></span>

## <span data-ttu-id="aa411-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa411-149">RELATED LINKS</span></span>