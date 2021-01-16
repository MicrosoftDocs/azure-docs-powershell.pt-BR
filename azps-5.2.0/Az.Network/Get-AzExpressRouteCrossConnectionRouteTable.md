---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257668"
---
# <span data-ttu-id="4a3c6-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4a3c6-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="4a3c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3c6-103">Obtém uma tabela de rota de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="4a3c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a3c6-104">SYNTAX</span></span>

### <span data-ttu-id="4a3c6-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="4a3c6-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a3c6-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="4a3c6-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a3c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a3c6-107">DESCRIPTION</span></span>
<span data-ttu-id="4a3c6-108">O cmdlet **Get-AzExpressRouteCrossConnectionRouteTable** recupera uma tabela de rotas detalhadas de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="4a3c6-109">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="4a3c6-110">Você pode usar a tabela de rotas para validar a configuração e a conectividade de pares.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="4a3c6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-111">EXAMPLES</span></span>

### <span data-ttu-id="4a3c6-112">Exemplo 1: exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="4a3c6-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="4a3c6-113">OS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-113">PARAMETERS</span></span>

### <span data-ttu-id="4a3c6-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-114">-CrossConnectionName</span></span>
<span data-ttu-id="4a3c6-115">O nome da conexão cruzada de rota expressa</span><span class="sxs-lookup"><span data-stu-id="4a3c6-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3c6-116">-DefaultProfile</span></span>
<span data-ttu-id="4a3c6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3c6-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4a3c6-118">-DevicePath</span></span>
<span data-ttu-id="4a3c6-119">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4a3c6-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4a3c6-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="4a3c6-121">A conexão cruzada de rota expressa</span><span class="sxs-lookup"><span data-stu-id="4a3c6-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4a3c6-122">-PeeringType</span></span>
<span data-ttu-id="4a3c6-123">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4a3c6-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a3c6-125">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3c6-126">CommonParameters</span></span>
<span data-ttu-id="4a3c6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3c6-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3c6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a3c6-129">INPUTS</span></span>

### <span data-ttu-id="4a3c6-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4a3c6-130">None</span></span>
<span data-ttu-id="4a3c6-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a3c6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a3c6-132">OUTPUTS</span></span>

### <span data-ttu-id="4a3c6-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="4a3c6-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="4a3c6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a3c6-134">NOTES</span></span>

## <span data-ttu-id="4a3c6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="4a3c6-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="4a3c6-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="4a3c6-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4a3c6-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
