---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 04c4355caaa76776a96e2619a0080b9c32d8e98a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402075"
---
# <span data-ttu-id="1ce72-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1ce72-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="1ce72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ce72-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce72-103">Obtém a tabela ARP de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ce72-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1ce72-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ce72-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ce72-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ce72-105">DESCRIPTION</span></span>
<span data-ttu-id="1ce72-106">O cmdlet **Get-AzExpressRoute CircuitARPTable** recupera a tabela ARP de ambas as interfaces de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ce72-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="1ce72-107">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um ponto específico.</span><span class="sxs-lookup"><span data-stu-id="1ce72-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="1ce72-108">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="1ce72-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="1ce72-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ce72-109">EXAMPLES</span></span>

### <span data-ttu-id="1ce72-110">Exemplo 1: Exibir a tabela ARP para um ponto do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1ce72-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="1ce72-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ce72-111">PARAMETERS</span></span>

### <span data-ttu-id="1ce72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce72-112">-DefaultProfile</span></span>
<span data-ttu-id="1ce72-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1ce72-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce72-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1ce72-114">-DevicePath</span></span>
<span data-ttu-id="1ce72-115">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1ce72-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1ce72-116">-ExpressRoute CircuitName</span><span class="sxs-lookup"><span data-stu-id="1ce72-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="1ce72-117">O nome do circuito do ExpressRoute que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="1ce72-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce72-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1ce72-118">-PeeringType</span></span>
<span data-ttu-id="1ce72-119">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1ce72-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1ce72-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce72-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ce72-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ce72-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce72-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce72-122">CommonParameters</span></span>
<span data-ttu-id="1ce72-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce72-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce72-124">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ce72-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce72-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ce72-125">INPUTS</span></span>

### <span data-ttu-id="1ce72-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1ce72-126">System.String</span></span>

## <span data-ttu-id="1ce72-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ce72-127">OUTPUTS</span></span>

### <span data-ttu-id="1ce72-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="1ce72-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="1ce72-129">Notas</span><span class="sxs-lookup"><span data-stu-id="1ce72-129">NOTES</span></span>

## <span data-ttu-id="1ce72-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ce72-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ce72-131">Get-AzExpressRoute CircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ce72-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1ce72-132">Get-AzExpressRoute CircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ce72-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="1ce72-133">Get-AzExpressRoute CircuitStat</span><span class="sxs-lookup"><span data-stu-id="1ce72-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
