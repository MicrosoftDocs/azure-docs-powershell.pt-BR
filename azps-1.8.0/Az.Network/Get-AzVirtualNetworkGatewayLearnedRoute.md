---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 80bb8e05b110f1b3e9689895ae9bea2aad1207b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600470"
---
# <span data-ttu-id="879ae-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="879ae-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="879ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="879ae-102">SYNOPSIS</span></span>
<span data-ttu-id="879ae-103">Lista rotas aprendidas por um gateway virtual de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="879ae-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="879ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="879ae-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="879ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="879ae-105">DESCRIPTION</span></span>
<span data-ttu-id="879ae-106">Enumera rotas aprendidas por um gateway virtual de rede do Azure de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="879ae-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="879ae-107">Isso inclui rotas aprendidas pelo BGP, bem como rotas estáticas.</span><span class="sxs-lookup"><span data-stu-id="879ae-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="879ae-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="879ae-108">EXAMPLES</span></span>

### <span data-ttu-id="879ae-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="879ae-109">Example 1</span></span>
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

<span data-ttu-id="879ae-110">Para o gateway de rede virtual do Azure chamado GATEWAYNAME no grupo de Resource do grupo de recursos, recupera rotas que o gateway do Azure sabe.</span><span class="sxs-lookup"><span data-stu-id="879ae-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="879ae-111">Nesse caso, o gateway de rede virtual do Azure tem duas rotas estáticas (10.1.0.0/16 e 10.0.0.254/32), bem como uma rota aprendida pelo BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="879ae-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="879ae-112">OS</span><span class="sxs-lookup"><span data-stu-id="879ae-112">PARAMETERS</span></span>

### <span data-ttu-id="879ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="879ae-113">-AsJob</span></span>
<span data-ttu-id="879ae-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="879ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="879ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879ae-115">-DefaultProfile</span></span>
<span data-ttu-id="879ae-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="879ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="879ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="879ae-118">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="879ae-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="879ae-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="879ae-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="879ae-120">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="879ae-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="879ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879ae-121">CommonParameters</span></span>
<span data-ttu-id="879ae-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="879ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879ae-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="879ae-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879ae-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="879ae-124">INPUTS</span></span>

### <span data-ttu-id="879ae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="879ae-125">System.String</span></span>

## <span data-ttu-id="879ae-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="879ae-126">OUTPUTS</span></span>

### <span data-ttu-id="879ae-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="879ae-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="879ae-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="879ae-128">NOTES</span></span>

## <span data-ttu-id="879ae-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="879ae-129">RELATED LINKS</span></span>
