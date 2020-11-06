---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: ce1e05106350adda37ffa5877585ff37337dad87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600603"
---
# <span data-ttu-id="56d60-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="56d60-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="56d60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56d60-102">SYNOPSIS</span></span>
<span data-ttu-id="56d60-103">Obtém a tabela ARP de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56d60-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="56d60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56d60-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56d60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56d60-105">DESCRIPTION</span></span>
<span data-ttu-id="56d60-106">O cmdlet **Get-AzExpressRouteCircuitARPTable** recupera a tabela ARP de ambas as interfaces de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56d60-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="56d60-107">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="56d60-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="56d60-108">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="56d60-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="56d60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56d60-109">EXAMPLES</span></span>

### <span data-ttu-id="56d60-110">Exemplo 1: exibir a tabela ARP para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="56d60-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="56d60-111">OS</span><span class="sxs-lookup"><span data-stu-id="56d60-111">PARAMETERS</span></span>

### <span data-ttu-id="56d60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d60-112">-DefaultProfile</span></span>
<span data-ttu-id="56d60-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56d60-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d60-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="56d60-114">-DevicePath</span></span>
<span data-ttu-id="56d60-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="56d60-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="56d60-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="56d60-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="56d60-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="56d60-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="56d60-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="56d60-118">-PeeringType</span></span>
<span data-ttu-id="56d60-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="56d60-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="56d60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d60-120">-ResourceGroupName</span></span>
<span data-ttu-id="56d60-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56d60-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="56d60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d60-122">CommonParameters</span></span>
<span data-ttu-id="56d60-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d60-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d60-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d60-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56d60-125">INPUTS</span></span>

### <span data-ttu-id="56d60-126">System. String</span><span class="sxs-lookup"><span data-stu-id="56d60-126">System.String</span></span>

## <span data-ttu-id="56d60-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56d60-127">OUTPUTS</span></span>

### <span data-ttu-id="56d60-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="56d60-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="56d60-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56d60-129">NOTES</span></span>

## <span data-ttu-id="56d60-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d60-130">RELATED LINKS</span></span>

[<span data-ttu-id="56d60-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="56d60-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="56d60-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="56d60-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="56d60-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="56d60-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
