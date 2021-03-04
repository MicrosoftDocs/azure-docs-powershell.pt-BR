---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: 6980ccc3e3ad9c69755253183da1d83f522973da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892942"
---
# <span data-ttu-id="b8a6d-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a6d-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b8a6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a6d-103">Cria uma política de seletor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="b8a6d-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="b8a6d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8a6d-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a6d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a6d-106">O New-AzTrafficSelectorPolicy cmdlet cria uma proposta de política de seletor de tráfego a ser usada em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b8a6d-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="b8a6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a6d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8a6d-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="b8a6d-109">Cria uma instância de uma política de seletor de tráfego e a adiciona como parâmetro ao criar uma conexão de gateway de rede virtual com um protocolo IKEv2.</span><span class="sxs-lookup"><span data-stu-id="b8a6d-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="b8a6d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8a6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a6d-111">-DefaultProfile</span></span>
<span data-ttu-id="b8a6d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a6d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a6d-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="b8a6d-113">-LocalAddressRange</span></span>
<span data-ttu-id="b8a6d-114">Uma coleção de intervalos de endereços CIDR</span><span class="sxs-lookup"><span data-stu-id="b8a6d-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6d-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="b8a6d-115">-RemoteAddressRange</span></span>
<span data-ttu-id="b8a6d-116">Uma coleção de intervalos de endereços CIDR</span><span class="sxs-lookup"><span data-stu-id="b8a6d-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a6d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a6d-117">CommonParameters</span></span>
<span data-ttu-id="b8a6d-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a6d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a6d-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8a6d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a6d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-120">INPUTS</span></span>

### <span data-ttu-id="b8a6d-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b8a6d-121">System.String[]</span></span>

## <span data-ttu-id="b8a6d-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-122">OUTPUTS</span></span>

### <span data-ttu-id="b8a6d-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b8a6d-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b8a6d-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8a6d-124">NOTES</span></span>

## <span data-ttu-id="b8a6d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8a6d-125">RELATED LINKS</span></span>
