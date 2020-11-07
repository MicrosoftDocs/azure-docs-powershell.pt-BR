---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: d235a43e4b5f2bcec2e93a9dfda4860588647179
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775464"
---
# <span data-ttu-id="b28c1-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="b28c1-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="b28c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b28c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b28c1-103">Lista rotas aprendidas por um gateway virtual de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="b28c1-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="b28c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b28c1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b28c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b28c1-105">DESCRIPTION</span></span>
<span data-ttu-id="b28c1-106">Enumera rotas aprendidas por um gateway virtual de rede do Azure de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="b28c1-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="b28c1-107">Isso inclui rotas aprendidas pelo BGP, bem como rotas estáticas.</span><span class="sxs-lookup"><span data-stu-id="b28c1-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="b28c1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b28c1-108">EXAMPLES</span></span>

### <span data-ttu-id="b28c1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b28c1-109">Example 1</span></span>
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

<span data-ttu-id="b28c1-110">Para o gateway de rede virtual do Azure chamado GATEWAYNAME no grupo de Resource do grupo de recursos, recupera rotas que o gateway do Azure sabe.</span><span class="sxs-lookup"><span data-stu-id="b28c1-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="b28c1-111">Nesse caso, o gateway de rede virtual do Azure tem duas rotas estáticas (10.1.0.0/16 e 10.0.0.254/32), bem como uma rota aprendida pelo BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="b28c1-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="b28c1-112">OS</span><span class="sxs-lookup"><span data-stu-id="b28c1-112">PARAMETERS</span></span>

### <span data-ttu-id="b28c1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b28c1-113">-AsJob</span></span>
<span data-ttu-id="b28c1-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b28c1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28c1-115">-DefaultProfile</span></span>
<span data-ttu-id="b28c1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b28c1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b28c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="b28c1-118">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b28c1-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="b28c1-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b28c1-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b28c1-120">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b28c1-120">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b28c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28c1-121">CommonParameters</span></span>
<span data-ttu-id="b28c1-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28c1-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28c1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28c1-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b28c1-124">INPUTS</span></span>

### <span data-ttu-id="b28c1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b28c1-125">System.String</span></span>

## <span data-ttu-id="b28c1-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b28c1-126">OUTPUTS</span></span>

### <span data-ttu-id="b28c1-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="b28c1-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="b28c1-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b28c1-128">NOTES</span></span>

## <span data-ttu-id="b28c1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b28c1-129">RELATED LINKS</span></span>
