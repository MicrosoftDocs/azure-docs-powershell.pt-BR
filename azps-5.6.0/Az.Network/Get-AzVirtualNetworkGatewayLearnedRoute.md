---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 8dbc1ad62d11ac6b14897c27b11ebdb7f6fb8cc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886443"
---
# <span data-ttu-id="cfaa5-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="cfaa5-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="cfaa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaa5-103">Lista as rotas aprendidas por um gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="cfaa5-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="cfaa5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cfaa5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfaa5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cfaa5-105">DESCRIPTION</span></span>
<span data-ttu-id="cfaa5-106">Enumera rotas aprendidas por um gateway de rede virtual do Azure de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="cfaa5-107">Isso inclui rotas aprendidas sobre BGP, bem como rotas estáticas.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="cfaa5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-108">EXAMPLES</span></span>

### <span data-ttu-id="cfaa5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfaa5-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="cfaa5-110">Para o gateway de rede virtual do Azure chamado gatewayname no resourceGroup do grupo de recursos, recupera rotas que o gateway do Azure conhece.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="cfaa5-111">O gateway de rede virtual do Azure nesse caso tem duas rotas estáticas (10.1.0.0/16 e 10.0.0.254/32), bem como uma rota aprendida sobre bgp (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="cfaa5-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="cfaa5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-112">PARAMETERS</span></span>

### <span data-ttu-id="cfaa5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfaa5-113">-AsJob</span></span>
<span data-ttu-id="cfaa5-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cfaa5-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaa5-115">-DefaultProfile</span></span>
<span data-ttu-id="cfaa5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfaa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfaa5-118">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="cfaa5-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="cfaa5-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cfaa5-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cfaa5-120">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="cfaa5-120">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaa5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaa5-121">CommonParameters</span></span>
<span data-ttu-id="cfaa5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaa5-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfaa5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaa5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-124">INPUTS</span></span>

### <span data-ttu-id="cfaa5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="cfaa5-125">System.String</span></span>

## <span data-ttu-id="cfaa5-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-126">OUTPUTS</span></span>

### <span data-ttu-id="cfaa5-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="cfaa5-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="cfaa5-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="cfaa5-128">NOTES</span></span>

## <span data-ttu-id="cfaa5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfaa5-129">RELATED LINKS</span></span>
