---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428991"
---
# <span data-ttu-id="89b4c-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="89b4c-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="89b4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="89b4c-103">Lista rotas aprendidas por um gateway virtual de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="89b4c-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="89b4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89b4c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="89b4c-106">Enumera rotas aprendidas por um gateway virtual de rede do Azure de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="89b4c-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="89b4c-107">Isso inclui rotas aprendidas pelo BGP, bem como rotas estáticas.</span><span class="sxs-lookup"><span data-stu-id="89b4c-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="89b4c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89b4c-108">EXAMPLES</span></span>

### <span data-ttu-id="89b4c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89b4c-109">Example 1</span></span>
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

<span data-ttu-id="89b4c-110">Para o gateway de rede virtual do Azure chamado GATEWAYNAME no grupo de Resource do grupo de recursos, recupera rotas que o gateway do Azure sabe.</span><span class="sxs-lookup"><span data-stu-id="89b4c-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="89b4c-111">Nesse caso, o gateway de rede virtual do Azure tem duas rotas estáticas (10.1.0.0/16 e 10.0.0.254/32), bem como uma rota aprendida pelo BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="89b4c-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="89b4c-112">OS</span><span class="sxs-lookup"><span data-stu-id="89b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="89b4c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89b4c-113">-AsJob</span></span>
<span data-ttu-id="89b4c-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89b4c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89b4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b4c-115">-DefaultProfile</span></span>
<span data-ttu-id="89b4c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89b4c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="89b4c-118">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="89b4c-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="89b4c-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="89b4c-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="89b4c-120">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="89b4c-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="89b4c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b4c-121">CommonParameters</span></span>
<span data-ttu-id="89b4c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b4c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b4c-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89b4c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b4c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89b4c-124">INPUTS</span></span>

### <span data-ttu-id="89b4c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="89b4c-125">System.String</span></span>

## <span data-ttu-id="89b4c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89b4c-126">OUTPUTS</span></span>

### <span data-ttu-id="89b4c-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="89b4c-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="89b4c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89b4c-128">NOTES</span></span>

## <span data-ttu-id="89b4c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89b4c-129">RELATED LINKS</span></span>
