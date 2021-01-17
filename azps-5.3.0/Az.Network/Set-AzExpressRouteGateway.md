---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433409"
---
# <span data-ttu-id="d7838-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d7838-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="d7838-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7838-102">SYNOPSIS</span></span>
<span data-ttu-id="d7838-103">Atualiza um gateway ExpressRoute dimensionável.</span><span class="sxs-lookup"><span data-stu-id="d7838-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="d7838-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7838-104">SYNTAX</span></span>

### <span data-ttu-id="d7838-105">ByExpressRouteGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7838-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7838-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d7838-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7838-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d7838-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7838-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7838-108">DESCRIPTION</span></span>

<span data-ttu-id="d7838-109">O cmdlet **set-AzExpressRouteGateway** permite que você atualize as unidades de escala de um ExpressRouteGateway existente ou atualize as marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="d7838-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="d7838-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7838-110">EXAMPLES</span></span>

### <span data-ttu-id="d7838-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7838-111">Example 1</span></span>

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

<span data-ttu-id="d7838-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7838-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d7838-113">Um gateway do ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala que serão modificadas para 3 unidades de escala</span><span class="sxs-lookup"><span data-stu-id="d7838-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="d7838-114">OS</span><span class="sxs-lookup"><span data-stu-id="d7838-114">PARAMETERS</span></span>

### <span data-ttu-id="d7838-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7838-115">-AsJob</span></span>
<span data-ttu-id="d7838-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7838-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7838-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7838-117">-DefaultProfile</span></span>
<span data-ttu-id="d7838-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7838-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7838-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7838-119">-InputObject</span></span>
<span data-ttu-id="d7838-120">O ExpressRouteGateway que precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d7838-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="d7838-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d7838-121">-MaxScaleUnits</span></span>
<span data-ttu-id="d7838-122">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="d7838-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d7838-123">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="d7838-123">Valid range > 2</span></span>

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

### <span data-ttu-id="d7838-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d7838-124">-MinScaleUnits</span></span>
<span data-ttu-id="d7838-125">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="d7838-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d7838-126">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="d7838-126">Valid range > 2</span></span>

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

### <span data-ttu-id="d7838-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7838-127">-Name</span></span>
<span data-ttu-id="d7838-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d7838-128">The resource name.</span></span>

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

### <span data-ttu-id="d7838-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7838-129">-ResourceGroupName</span></span>
<span data-ttu-id="d7838-130">O nome do grupo de recursos do ExpressRouteGateway a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d7838-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="d7838-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7838-131">-ResourceId</span></span>
<span data-ttu-id="d7838-132">A ID do ExpressRouteGateway que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d7838-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="d7838-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="d7838-133">-Tag</span></span>
<span data-ttu-id="d7838-134">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7838-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d7838-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7838-135">-Confirm</span></span>
<span data-ttu-id="d7838-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7838-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7838-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7838-137">-WhatIf</span></span>
<span data-ttu-id="d7838-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7838-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7838-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7838-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7838-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7838-140">CommonParameters</span></span>
<span data-ttu-id="d7838-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7838-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7838-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7838-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7838-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7838-143">INPUTS</span></span>

### <span data-ttu-id="d7838-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d7838-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d7838-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d7838-145">System.String</span></span>

## <span data-ttu-id="d7838-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7838-146">OUTPUTS</span></span>

### <span data-ttu-id="d7838-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d7838-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="d7838-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7838-148">NOTES</span></span>

## <span data-ttu-id="d7838-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7838-149">RELATED LINKS</span></span>
