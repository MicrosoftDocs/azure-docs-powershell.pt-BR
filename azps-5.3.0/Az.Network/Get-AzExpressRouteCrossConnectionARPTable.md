---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427022"
---
# <span data-ttu-id="85855-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="85855-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="85855-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85855-102">SYNOPSIS</span></span>
<span data-ttu-id="85855-103">Obtém a tabela ARP de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85855-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="85855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85855-104">SYNTAX</span></span>

### <span data-ttu-id="85855-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="85855-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85855-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="85855-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85855-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85855-107">DESCRIPTION</span></span>
<span data-ttu-id="85855-108">O cmdlet **Get-AzExpressRouteCrossConnectionARPTable** recupera a tabela ARP de ambas as interfaces de uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85855-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="85855-109">A tabela ARP fornece um mapeamento do endereço IPv4 para o endereço MAC para um emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="85855-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="85855-110">Você pode usar a tabela ARP para validar a configuração e a conectividade da camada 2.</span><span class="sxs-lookup"><span data-stu-id="85855-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="85855-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85855-111">EXAMPLES</span></span>

### <span data-ttu-id="85855-112">Exemplo 1: exibir a tabela ARP para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="85855-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="85855-113">OS</span><span class="sxs-lookup"><span data-stu-id="85855-113">PARAMETERS</span></span>

### <span data-ttu-id="85855-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="85855-114">-CrossConnectionName</span></span>
<span data-ttu-id="85855-115">O nome da conexão cruzada de rota expressa</span><span class="sxs-lookup"><span data-stu-id="85855-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="85855-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85855-116">-DefaultProfile</span></span>
<span data-ttu-id="85855-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85855-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85855-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="85855-118">-DevicePath</span></span>
<span data-ttu-id="85855-119">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="85855-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="85855-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="85855-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="85855-121">A conexão cruzada de rota expressa</span><span class="sxs-lookup"><span data-stu-id="85855-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="85855-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="85855-122">-PeeringType</span></span>
<span data-ttu-id="85855-123">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="85855-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="85855-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85855-124">-ResourceGroupName</span></span>
<span data-ttu-id="85855-125">O nome do grupo de recursos que contém a conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85855-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="85855-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85855-126">CommonParameters</span></span>
<span data-ttu-id="85855-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85855-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85855-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85855-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85855-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85855-129">INPUTS</span></span>

### <span data-ttu-id="85855-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85855-130">None</span></span>
<span data-ttu-id="85855-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="85855-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85855-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85855-132">OUTPUTS</span></span>

### <span data-ttu-id="85855-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="85855-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="85855-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85855-134">NOTES</span></span>

## <span data-ttu-id="85855-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85855-135">RELATED LINKS</span></span>

[<span data-ttu-id="85855-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="85855-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="85855-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="85855-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
