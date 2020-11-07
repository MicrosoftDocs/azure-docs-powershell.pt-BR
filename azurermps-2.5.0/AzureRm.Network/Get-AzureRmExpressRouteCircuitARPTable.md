---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785510"
---
# <span data-ttu-id="b6c62-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b6c62-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="b6c62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6c62-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c62-103">Obtém a tabela ARP de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b6c62-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6c62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6c62-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6c62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6c62-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c62-106">O cmdlet **Get-AzureRmExpressRouteCircuitARPTable** recupera a tabela ARP de ambas as interfaces de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b6c62-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="b6c62-107">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="b6c62-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="b6c62-108">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="b6c62-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="b6c62-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6c62-109">EXAMPLES</span></span>

### <span data-ttu-id="b6c62-110">Exemplo 1: exibir a tabela ARP para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b6c62-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="b6c62-111">OS</span><span class="sxs-lookup"><span data-stu-id="b6c62-111">PARAMETERS</span></span>

### <span data-ttu-id="b6c62-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c62-112">-DefaultProfile</span></span>
<span data-ttu-id="b6c62-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c62-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c62-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b6c62-114">-DevicePath</span></span>
<span data-ttu-id="b6c62-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b6c62-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c62-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="b6c62-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b6c62-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="b6c62-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c62-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b6c62-118">-PeeringType</span></span>
<span data-ttu-id="b6c62-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b6c62-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c62-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6c62-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b6c62-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c62-122">CommonParameters</span></span>
<span data-ttu-id="b6c62-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c62-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c62-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6c62-125">INPUTS</span></span>

## <span data-ttu-id="b6c62-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6c62-126">OUTPUTS</span></span>

### <span data-ttu-id="b6c62-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="b6c62-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="b6c62-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6c62-128">NOTES</span></span>

## <span data-ttu-id="b6c62-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6c62-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6c62-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6c62-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b6c62-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6c62-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b6c62-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="b6c62-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
