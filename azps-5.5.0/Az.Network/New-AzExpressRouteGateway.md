---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112845"
---
# <span data-ttu-id="b9146-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b9146-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="b9146-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9146-102">SYNOPSIS</span></span>
<span data-ttu-id="b9146-103">Cria um Gateway escalonável do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b9146-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="b9146-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9146-104">SYNTAX</span></span>

### <span data-ttu-id="b9146-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9146-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9146-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b9146-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9146-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b9146-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9146-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9146-108">DESCRIPTION</span></span>

<span data-ttu-id="b9146-109">New-AzExpressRouteGateway cria um Gateway escalonável do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b9146-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="b9146-110">Essa é a conectividade definida pelo software para o Azure local dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b9146-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="b9146-111">Esse gateway pode ser dimensionado com base na unidade de escala especificada nesta ou no cmdlet Set-AzExpressRouteGateway dados.</span><span class="sxs-lookup"><span data-stu-id="b9146-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="b9146-112">Uma conexão é configurada de um circuito local do ExpressRoute para o gateway escalável.</span><span class="sxs-lookup"><span data-stu-id="b9146-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="b9146-113">O ExpressRouteGateway estará no mesmo local que o VirtualHub referenciado.</span><span class="sxs-lookup"><span data-stu-id="b9146-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="b9146-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9146-114">EXAMPLES</span></span>

### <span data-ttu-id="b9146-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9146-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b9146-116">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="b9146-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b9146-117">Um gateway do ExpressRoute será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="b9146-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="b9146-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9146-118">PARAMETERS</span></span>

### <span data-ttu-id="b9146-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9146-119">-AsJob</span></span>
<span data-ttu-id="b9146-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b9146-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9146-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9146-121">-DefaultProfile</span></span>
<span data-ttu-id="b9146-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9146-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9146-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="b9146-123">-MaxScaleUnits</span></span>
<span data-ttu-id="b9146-124">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="b9146-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="b9146-125">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="b9146-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="b9146-126">-MinScaleUnits</span></span>
<span data-ttu-id="b9146-127">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="b9146-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="b9146-128">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="b9146-128">Valid range > 2</span></span>

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

### <span data-ttu-id="b9146-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9146-129">-Name</span></span>
<span data-ttu-id="b9146-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9146-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9146-131">-ResourceGroupName</span></span>
<span data-ttu-id="b9146-132">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9146-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9146-133">-Tag</span></span>
<span data-ttu-id="b9146-134">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b9146-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b9146-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b9146-135">-VirtualHub</span></span>
<span data-ttu-id="b9146-136">O VirtualHub a que este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="b9146-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="b9146-137">-VirtualHubId</span></span>
<span data-ttu-id="b9146-138">A ID do VirtualHub a que este VpnGateway precisa estar associada.</span><span class="sxs-lookup"><span data-stu-id="b9146-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="b9146-139">-VirtualHubName</span></span>
<span data-ttu-id="b9146-140">A ID do VirtualHub a que este VpnGateway precisa estar associada.</span><span class="sxs-lookup"><span data-stu-id="b9146-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9146-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b9146-141">-Confirm</span></span>
<span data-ttu-id="b9146-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9146-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9146-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9146-143">-WhatIf</span></span>
<span data-ttu-id="b9146-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b9146-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9146-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9146-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9146-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9146-146">CommonParameters</span></span>
<span data-ttu-id="b9146-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9146-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9146-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9146-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9146-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9146-149">INPUTS</span></span>

### <span data-ttu-id="b9146-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b9146-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b9146-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b9146-151">System.String</span></span>

## <span data-ttu-id="b9146-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9146-152">OUTPUTS</span></span>

### <span data-ttu-id="b9146-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b9146-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="b9146-154">Notas</span><span class="sxs-lookup"><span data-stu-id="b9146-154">NOTES</span></span>

## <span data-ttu-id="b9146-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9146-155">RELATED LINKS</span></span>
