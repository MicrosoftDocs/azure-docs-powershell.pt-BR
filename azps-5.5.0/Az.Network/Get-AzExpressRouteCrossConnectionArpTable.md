---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
ms.openlocfilehash: 8dac5f65599ead696416eaf33f8773415a5631cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113516"
---
# <span data-ttu-id="98083-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="98083-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="98083-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98083-102">SYNOPSIS</span></span>
<span data-ttu-id="98083-103">Obtém a tabela ARP de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="98083-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="98083-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98083-104">SYNTAX</span></span>

### <span data-ttu-id="98083-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="98083-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98083-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="98083-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98083-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="98083-107">DESCRIPTION</span></span>
<span data-ttu-id="98083-108">O cmdlet **Get-AzExpressRouteCrossConnectionARPTable** recupera a tabela ARP de ambas as interfaces de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="98083-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="98083-109">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um ponto específico.</span><span class="sxs-lookup"><span data-stu-id="98083-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="98083-110">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="98083-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="98083-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98083-111">EXAMPLES</span></span>

### <span data-ttu-id="98083-112">Exemplo 1: Exibir a tabela ARP para um ponto do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="98083-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="98083-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98083-113">PARAMETERS</span></span>

### <span data-ttu-id="98083-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="98083-114">-CrossConnectionName</span></span>
<span data-ttu-id="98083-115">O nome da Conexão Cruzada de Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="98083-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="98083-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98083-116">-DefaultProfile</span></span>
<span data-ttu-id="98083-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="98083-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98083-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="98083-118">-DevicePath</span></span>
<span data-ttu-id="98083-119">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="98083-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="98083-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="98083-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="98083-121">A Conexão Cruzada de Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="98083-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="98083-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="98083-122">-PeeringType</span></span>
<span data-ttu-id="98083-123">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="98083-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="98083-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98083-124">-ResourceGroupName</span></span>
<span data-ttu-id="98083-125">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="98083-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="98083-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98083-126">CommonParameters</span></span>
<span data-ttu-id="98083-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98083-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98083-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98083-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98083-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="98083-129">INPUTS</span></span>

### <span data-ttu-id="98083-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="98083-130">None</span></span>
<span data-ttu-id="98083-131">Este cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="98083-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98083-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="98083-132">OUTPUTS</span></span>

### <span data-ttu-id="98083-133">Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="98083-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="98083-134">Notas</span><span class="sxs-lookup"><span data-stu-id="98083-134">NOTES</span></span>

## <span data-ttu-id="98083-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98083-135">RELATED LINKS</span></span>

[<span data-ttu-id="98083-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="98083-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="98083-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="98083-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
