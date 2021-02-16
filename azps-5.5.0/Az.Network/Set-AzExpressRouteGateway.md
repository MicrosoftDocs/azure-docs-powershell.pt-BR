---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118264"
---
# <span data-ttu-id="5bd56-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5bd56-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="5bd56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bd56-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd56-103">Atualiza um Gateway escalonável do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5bd56-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="5bd56-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd56-104">SYNTAX</span></span>

### <span data-ttu-id="5bd56-105">ByExpressRouteGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5bd56-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd56-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="5bd56-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bd56-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5bd56-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd56-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bd56-108">DESCRIPTION</span></span>

<span data-ttu-id="5bd56-109">O cmdlet **Set-AzExpressRouteGateway** permite que você atualize as unidades de escala de um ExpressRouteGateway existente ou atualize as marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="5bd56-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="5bd56-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bd56-110">EXAMPLES</span></span>

### <span data-ttu-id="5bd56-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bd56-111">Example 1</span></span>

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

<span data-ttu-id="5bd56-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd56-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5bd56-113">Um gateway do ExpressRoute será criado posteriormente no Hub Virtual com 2 unidades de escala que serão modificadas para 3 unidades de escala</span><span class="sxs-lookup"><span data-stu-id="5bd56-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="5bd56-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bd56-114">PARAMETERS</span></span>

### <span data-ttu-id="5bd56-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bd56-115">-AsJob</span></span>
<span data-ttu-id="5bd56-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5bd56-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bd56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd56-117">-DefaultProfile</span></span>
<span data-ttu-id="5bd56-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd56-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bd56-119">-InputObject</span></span>
<span data-ttu-id="5bd56-120">O ExpressRouteGateway que precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5bd56-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="5bd56-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="5bd56-121">-MaxScaleUnits</span></span>
<span data-ttu-id="5bd56-122">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="5bd56-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="5bd56-123">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="5bd56-123">Valid range > 2</span></span>

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

### <span data-ttu-id="5bd56-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="5bd56-124">-MinScaleUnits</span></span>
<span data-ttu-id="5bd56-125">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="5bd56-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="5bd56-126">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="5bd56-126">Valid range > 2</span></span>

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

### <span data-ttu-id="5bd56-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bd56-127">-Name</span></span>
<span data-ttu-id="5bd56-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5bd56-128">The resource name.</span></span>

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

### <span data-ttu-id="5bd56-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd56-129">-ResourceGroupName</span></span>
<span data-ttu-id="5bd56-130">O nome do grupo de recursos do ExpressRouteGateway a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5bd56-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="5bd56-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bd56-131">-ResourceId</span></span>
<span data-ttu-id="5bd56-132">A ID do ExpressRouteGateway que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="5bd56-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="5bd56-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bd56-133">-Tag</span></span>
<span data-ttu-id="5bd56-134">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="5bd56-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5bd56-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5bd56-135">-Confirm</span></span>
<span data-ttu-id="5bd56-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd56-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd56-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd56-137">-WhatIf</span></span>
<span data-ttu-id="5bd56-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5bd56-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd56-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bd56-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd56-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd56-140">CommonParameters</span></span>
<span data-ttu-id="5bd56-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd56-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd56-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd56-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd56-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="5bd56-143">INPUTS</span></span>

### <span data-ttu-id="5bd56-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bd56-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5bd56-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5bd56-145">System.String</span></span>

## <span data-ttu-id="5bd56-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="5bd56-146">OUTPUTS</span></span>

### <span data-ttu-id="5bd56-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5bd56-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="5bd56-148">Notas</span><span class="sxs-lookup"><span data-stu-id="5bd56-148">NOTES</span></span>

## <span data-ttu-id="5bd56-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bd56-149">RELATED LINKS</span></span>
