---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 43bf5a0a551840d03ac19e9ea78b26135dde5493
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775560"
---
# <span data-ttu-id="17a21-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="17a21-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="17a21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17a21-102">SYNOPSIS</span></span>
<span data-ttu-id="17a21-103">Obtém a tabela ARP de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17a21-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="17a21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17a21-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17a21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17a21-105">DESCRIPTION</span></span>
<span data-ttu-id="17a21-106">O cmdlet **Get-AzExpressRouteCircuitARPTable** recupera a tabela ARP de ambas as interfaces de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17a21-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="17a21-107">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="17a21-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="17a21-108">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="17a21-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="17a21-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17a21-109">EXAMPLES</span></span>

### <span data-ttu-id="17a21-110">Exemplo 1: exibir a tabela ARP para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="17a21-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="17a21-111">OS</span><span class="sxs-lookup"><span data-stu-id="17a21-111">PARAMETERS</span></span>

### <span data-ttu-id="17a21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a21-112">-DefaultProfile</span></span>
<span data-ttu-id="17a21-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17a21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17a21-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="17a21-114">-DevicePath</span></span>
<span data-ttu-id="17a21-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="17a21-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="17a21-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="17a21-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="17a21-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="17a21-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="17a21-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="17a21-118">-PeeringType</span></span>
<span data-ttu-id="17a21-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="17a21-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="17a21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a21-120">-ResourceGroupName</span></span>
<span data-ttu-id="17a21-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17a21-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="17a21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a21-122">CommonParameters</span></span>
<span data-ttu-id="17a21-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a21-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a21-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a21-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17a21-125">INPUTS</span></span>

## <span data-ttu-id="17a21-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17a21-126">OUTPUTS</span></span>

### <span data-ttu-id="17a21-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="17a21-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="17a21-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17a21-128">NOTES</span></span>

## <span data-ttu-id="17a21-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17a21-129">RELATED LINKS</span></span>

[<span data-ttu-id="17a21-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a21-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="17a21-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="17a21-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="17a21-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="17a21-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
