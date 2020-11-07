---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942070"
---
# <span data-ttu-id="ce96a-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ce96a-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="ce96a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce96a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce96a-103">Cria um gateway ExpressRoute escalável.</span><span class="sxs-lookup"><span data-stu-id="ce96a-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="ce96a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce96a-104">SYNTAX</span></span>

### <span data-ttu-id="ce96a-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce96a-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce96a-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ce96a-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce96a-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ce96a-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce96a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce96a-108">DESCRIPTION</span></span>

<span data-ttu-id="ce96a-109">New-AzExpressRouteGateway cria um gateway de ExpressRoute escalável.</span><span class="sxs-lookup"><span data-stu-id="ce96a-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="ce96a-110">Esta é a conectividade definida por software para a premissation para o Azure dentro do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ce96a-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="ce96a-111">Esse gateway pode ser dimensionado com base na unidade de escala especificada nesse cmdlet ou Set-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ce96a-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="ce96a-112">Uma conexão é configurada a partir de um circuito do ExpressRoute no local para o gateway dimensionável.</span><span class="sxs-lookup"><span data-stu-id="ce96a-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="ce96a-113">O ExpressRouteGateway estará no mesmo local do VirtualHub referenciado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="ce96a-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce96a-114">EXAMPLES</span></span>

### <span data-ttu-id="ce96a-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce96a-115">Example 1</span></span>

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

<span data-ttu-id="ce96a-116">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce96a-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ce96a-117">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="ce96a-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="ce96a-118">OS</span><span class="sxs-lookup"><span data-stu-id="ce96a-118">PARAMETERS</span></span>

### <span data-ttu-id="ce96a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce96a-119">-AsJob</span></span>
<span data-ttu-id="ce96a-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ce96a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce96a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce96a-121">-DefaultProfile</span></span>
<span data-ttu-id="ce96a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce96a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce96a-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ce96a-123">-MaxScaleUnits</span></span>
<span data-ttu-id="ce96a-124">O número máximo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ce96a-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ce96a-125">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="ce96a-125">Valid range > 2</span></span>

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

### <span data-ttu-id="ce96a-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ce96a-126">-MinScaleUnits</span></span>
<span data-ttu-id="ce96a-127">O número mínimo de unidades de escala para este ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ce96a-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ce96a-128">Intervalo válido > 2</span><span class="sxs-lookup"><span data-stu-id="ce96a-128">Valid range > 2</span></span>

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

### <span data-ttu-id="ce96a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce96a-129">-Name</span></span>
<span data-ttu-id="ce96a-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce96a-130">The resource name.</span></span>

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

### <span data-ttu-id="ce96a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce96a-131">-ResourceGroupName</span></span>
<span data-ttu-id="ce96a-132">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce96a-132">The resource name.</span></span>

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

### <span data-ttu-id="ce96a-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="ce96a-133">-Tag</span></span>
<span data-ttu-id="ce96a-134">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce96a-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ce96a-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ce96a-135">-VirtualHub</span></span>
<span data-ttu-id="ce96a-136">O VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ce96a-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="ce96a-137">-VirtualHubId</span></span>
<span data-ttu-id="ce96a-138">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ce96a-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="ce96a-139">-VirtualHubName</span></span>
<span data-ttu-id="ce96a-140">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="ce96a-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce96a-141">-Confirm</span></span>
<span data-ttu-id="ce96a-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce96a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce96a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce96a-143">-WhatIf</span></span>
<span data-ttu-id="ce96a-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce96a-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce96a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce96a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce96a-146">CommonParameters</span></span>
<span data-ttu-id="ce96a-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce96a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce96a-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce96a-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce96a-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce96a-149">INPUTS</span></span>

### <span data-ttu-id="ce96a-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ce96a-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ce96a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ce96a-151">System.String</span></span>

## <span data-ttu-id="ce96a-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce96a-152">OUTPUTS</span></span>

### <span data-ttu-id="ce96a-153">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ce96a-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="ce96a-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce96a-154">NOTES</span></span>

## <span data-ttu-id="ce96a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce96a-155">RELATED LINKS</span></span>
