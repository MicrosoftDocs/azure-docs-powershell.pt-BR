---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 12c920d0bacc6bd214e6ebe8d374a80d2b50a072
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941381"
---
# <span data-ttu-id="c60ec-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c60ec-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="c60ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c60ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c60ec-103">Obtém a tabela ARP de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c60ec-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c60ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c60ec-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c60ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c60ec-105">DESCRIPTION</span></span>
<span data-ttu-id="c60ec-106">O cmdlet **Get-AzExpressRouteCircuitARPTable** recupera a tabela ARP de ambas as interfaces de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c60ec-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="c60ec-107">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="c60ec-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="c60ec-108">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="c60ec-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="c60ec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c60ec-109">EXAMPLES</span></span>

### <span data-ttu-id="c60ec-110">Exemplo 1: exibir a tabela ARP para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c60ec-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="c60ec-111">OS</span><span class="sxs-lookup"><span data-stu-id="c60ec-111">PARAMETERS</span></span>

### <span data-ttu-id="c60ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60ec-112">-DefaultProfile</span></span>
<span data-ttu-id="c60ec-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c60ec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c60ec-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c60ec-114">-DevicePath</span></span>
<span data-ttu-id="c60ec-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c60ec-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="c60ec-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c60ec-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c60ec-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="c60ec-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="c60ec-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c60ec-118">-PeeringType</span></span>
<span data-ttu-id="c60ec-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c60ec-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c60ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="c60ec-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c60ec-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="c60ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60ec-122">CommonParameters</span></span>
<span data-ttu-id="c60ec-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60ec-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c60ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60ec-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c60ec-125">INPUTS</span></span>

### <span data-ttu-id="c60ec-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c60ec-126">System.String</span></span>

## <span data-ttu-id="c60ec-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c60ec-127">OUTPUTS</span></span>

### <span data-ttu-id="c60ec-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="c60ec-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="c60ec-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c60ec-129">NOTES</span></span>

## <span data-ttu-id="c60ec-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c60ec-130">RELATED LINKS</span></span>

[<span data-ttu-id="c60ec-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c60ec-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c60ec-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c60ec-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c60ec-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c60ec-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
