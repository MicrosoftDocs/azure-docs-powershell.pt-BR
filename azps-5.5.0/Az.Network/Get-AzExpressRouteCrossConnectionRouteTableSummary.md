---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113511"
---
# <span data-ttu-id="9b66e-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9b66e-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="9b66e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b66e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b66e-103">Obtém um resumo da tabela de rota de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9b66e-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="9b66e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b66e-104">SYNTAX</span></span>

### <span data-ttu-id="9b66e-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="9b66e-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b66e-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="9b66e-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b66e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b66e-107">DESCRIPTION</span></span>
<span data-ttu-id="9b66e-108">O cmdlet **Get-AzExpressRouteCrossConnectionRouteTableSummary** recupera um resumo das informações do vizinhos BGP para um contexto de roteamento específico.</span><span class="sxs-lookup"><span data-stu-id="9b66e-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="9b66e-109">Essas informações são úteis para determinar por quanto tempo um contexto de roteamento foi estabelecido e o número de prefixos de rota anunciados pelo roteador de paridade.</span><span class="sxs-lookup"><span data-stu-id="9b66e-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="9b66e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9b66e-110">EXAMPLES</span></span>

### <span data-ttu-id="9b66e-111">Exemplo 1: Exibir o resumo da rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="9b66e-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="9b66e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b66e-112">PARAMETERS</span></span>

### <span data-ttu-id="9b66e-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="9b66e-113">-CrossConnectionName</span></span>
<span data-ttu-id="9b66e-114">O nome da Conexão Cruzada de Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="9b66e-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="9b66e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b66e-115">-DefaultProfile</span></span>
<span data-ttu-id="9b66e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9b66e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b66e-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="9b66e-117">-DevicePath</span></span>
<span data-ttu-id="9b66e-118">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="9b66e-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="9b66e-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9b66e-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="9b66e-120">A Conexão Cruzada de Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="9b66e-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="9b66e-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="9b66e-121">-PeeringType</span></span>
<span data-ttu-id="9b66e-122">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="9b66e-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="9b66e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b66e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b66e-124">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9b66e-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="9b66e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b66e-125">CommonParameters</span></span>
<span data-ttu-id="9b66e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b66e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b66e-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b66e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b66e-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="9b66e-128">INPUTS</span></span>

### <span data-ttu-id="9b66e-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9b66e-129">None</span></span>
<span data-ttu-id="9b66e-130">Este cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9b66e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b66e-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="9b66e-131">OUTPUTS</span></span>

### <span data-ttu-id="9b66e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="9b66e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="9b66e-133">Notas</span><span class="sxs-lookup"><span data-stu-id="9b66e-133">NOTES</span></span>

## <span data-ttu-id="9b66e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b66e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b66e-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="9b66e-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="9b66e-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9b66e-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
