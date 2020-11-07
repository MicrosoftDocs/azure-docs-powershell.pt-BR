---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
ms.openlocfilehash: 0097cd022387b3ac2ee8ceb1fa2a831b60c4256d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785185"
---
# <span data-ttu-id="79e87-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="79e87-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="79e87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79e87-102">SYNOPSIS</span></span>
<span data-ttu-id="79e87-103">Lista rotas sendo anunciadas por um gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="79e87-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79e87-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79e87-105">DESCRIPTION</span></span>
<span data-ttu-id="79e87-106">Devido ao IP de um par BGP, enumera as rotas sendo anunciadas para esse ponto pelo gateway de rede virtual do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="79e87-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="79e87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79e87-107">EXAMPLES</span></span>

### <span data-ttu-id="79e87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79e87-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="79e87-109">Para o gateway do Azure chamado GATEWAYNAME na resourceGroupName do grupo de recursos, Retrives uma lista de rotas sendo anunciadas para o par BGP com IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="79e87-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="79e87-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="79e87-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="79e87-111">Para o gateway do Azure chamado GATEWAYNAME na lista de grupos de resourceGroupName, o recupera rotas sendo anunciadas para o primeiro par BGP na lista de pares BGP do gateway.</span><span class="sxs-lookup"><span data-stu-id="79e87-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="79e87-112">OS</span><span class="sxs-lookup"><span data-stu-id="79e87-112">PARAMETERS</span></span>

### <span data-ttu-id="79e87-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79e87-113">-AsJob</span></span>
<span data-ttu-id="79e87-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="79e87-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79e87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e87-115">-DefaultProfile</span></span>
<span data-ttu-id="79e87-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79e87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e87-117">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="79e87-117">-Peer</span></span>
<span data-ttu-id="79e87-118">Endereço IP do par BGP.</span><span class="sxs-lookup"><span data-stu-id="79e87-118">BGP peer's IP address.</span></span> <span data-ttu-id="79e87-119">Isso deve ser um IP dentro do espaço de endereço acessível de dentro da rede virtual do Azure na qual o gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="79e87-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="79e87-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e87-120">-ResourceGroupName</span></span>
<span data-ttu-id="79e87-121">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="79e87-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="79e87-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="79e87-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="79e87-123">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="79e87-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="79e87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e87-124">CommonParameters</span></span>
<span data-ttu-id="79e87-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e87-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e87-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79e87-127">INPUTS</span></span>

### <span data-ttu-id="79e87-128">System. String</span><span class="sxs-lookup"><span data-stu-id="79e87-128">System.String</span></span>

## <span data-ttu-id="79e87-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79e87-129">OUTPUTS</span></span>

### <span data-ttu-id="79e87-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="79e87-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="79e87-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79e87-131">NOTES</span></span>
<span data-ttu-id="79e87-132">Este comando somente é aplicável a gateways de rede virtual do Azure com conexões habilitadas para BGP.</span><span class="sxs-lookup"><span data-stu-id="79e87-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="79e87-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79e87-133">RELATED LINKS</span></span>

