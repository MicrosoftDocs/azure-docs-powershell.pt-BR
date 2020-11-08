---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111568"
---
# <span data-ttu-id="6cb76-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6cb76-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="6cb76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cb76-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb76-103">Cria uma política de seletor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6cb76-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="6cb76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cb76-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb76-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cb76-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb76-106">O cmdlet New-AzTrafficSelectorPolicy cria uma proposta de política de seletor de tráfego a ser usada em uma conexão de gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="6cb76-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="6cb76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cb76-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb76-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6cb76-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="6cb76-109">Cria uma instância de uma política de seletor de tráfego e a adiciona como um parâmetro ao criar uma conexão de gateway de rede virtual com um protocolo IKEv2.</span><span class="sxs-lookup"><span data-stu-id="6cb76-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="6cb76-110">OS</span><span class="sxs-lookup"><span data-stu-id="6cb76-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb76-111">-DefaultProfile</span></span>
<span data-ttu-id="6cb76-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb76-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="6cb76-113">-LocalAddressRange</span></span>
<span data-ttu-id="6cb76-114">Uma coleção de intervalos de endereços CIDR</span><span class="sxs-lookup"><span data-stu-id="6cb76-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="6cb76-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="6cb76-115">-RemoteAddressRange</span></span>
<span data-ttu-id="6cb76-116">Uma coleção de intervalos de endereços CIDR</span><span class="sxs-lookup"><span data-stu-id="6cb76-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="6cb76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb76-117">CommonParameters</span></span>
<span data-ttu-id="6cb76-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb76-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb76-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb76-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cb76-120">INPUTS</span></span>

### <span data-ttu-id="6cb76-121">System. String []</span><span class="sxs-lookup"><span data-stu-id="6cb76-121">System.String[]</span></span>

## <span data-ttu-id="6cb76-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cb76-122">OUTPUTS</span></span>

### <span data-ttu-id="6cb76-123">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6cb76-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="6cb76-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cb76-124">NOTES</span></span>

## <span data-ttu-id="6cb76-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cb76-125">RELATED LINKS</span></span>
