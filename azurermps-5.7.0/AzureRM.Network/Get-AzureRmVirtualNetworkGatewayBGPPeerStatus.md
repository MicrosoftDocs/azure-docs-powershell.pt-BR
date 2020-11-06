---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 66eaecd94c2275ff86af319a219c29f021100112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430979"
---
# <span data-ttu-id="5057b-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="5057b-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="5057b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5057b-102">SYNOPSIS</span></span>
<span data-ttu-id="5057b-103">Lista um par BGP do gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="5057b-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5057b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5057b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5057b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5057b-105">DESCRIPTION</span></span>
<span data-ttu-id="5057b-106">Este comando enumera pares BGP em que um gateway de rede virtual do Azure está configurado como ponto.</span><span class="sxs-lookup"><span data-stu-id="5057b-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="5057b-107">O status de cada par também é fornecido.</span><span class="sxs-lookup"><span data-stu-id="5057b-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="5057b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5057b-108">EXAMPLES</span></span>

### <span data-ttu-id="5057b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5057b-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="5057b-110">Recupera pares BGP para o gateway de rede virtual do Azure chamado GATEWAYNAME no grupo de Resource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5057b-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="5057b-111">Este exemplo de saída mostra um par BGP conectado, com um IP de 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="5057b-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="5057b-112">OS</span><span class="sxs-lookup"><span data-stu-id="5057b-112">PARAMETERS</span></span>

### <span data-ttu-id="5057b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5057b-113">-AsJob</span></span>
<span data-ttu-id="5057b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5057b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5057b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5057b-115">-DefaultProfile</span></span>
<span data-ttu-id="5057b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5057b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5057b-117">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="5057b-117">-Peer</span></span>
<span data-ttu-id="5057b-118">IP do par para recuperar o status de</span><span class="sxs-lookup"><span data-stu-id="5057b-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5057b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5057b-119">-ResourceGroupName</span></span>
<span data-ttu-id="5057b-120">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5057b-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="5057b-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5057b-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5057b-122">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5057b-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="5057b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5057b-123">CommonParameters</span></span>
<span data-ttu-id="5057b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5057b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5057b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5057b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5057b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5057b-126">INPUTS</span></span>

### <span data-ttu-id="5057b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5057b-127">System.String</span></span>

## <span data-ttu-id="5057b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5057b-128">OUTPUTS</span></span>

### <span data-ttu-id="5057b-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="5057b-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="5057b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5057b-130">NOTES</span></span>

## <span data-ttu-id="5057b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5057b-131">RELATED LINKS</span></span>
