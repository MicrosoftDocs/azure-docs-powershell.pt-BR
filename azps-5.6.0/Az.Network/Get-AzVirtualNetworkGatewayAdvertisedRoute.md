---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886922"
---
# <span data-ttu-id="03064-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="03064-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="03064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03064-102">SYNOPSIS</span></span>
<span data-ttu-id="03064-103">Lista as rotas que estão sendo anunciadas por um gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="03064-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="03064-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03064-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03064-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03064-105">DESCRIPTION</span></span>
<span data-ttu-id="03064-106">Dado o IP de um par BGP, enumera as rotas que estão sendo anunciadas para esse ponto pelo gateway de rede virtual do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="03064-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="03064-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03064-107">EXAMPLES</span></span>

### <span data-ttu-id="03064-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03064-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="03064-109">Para o gateway do Azure denominado gatewayName no resourceGroupName do grupo de recursos, recupera uma lista de rotas que estão sendo anunciadas para o par BGP com IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="03064-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="03064-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="03064-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="03064-111">Para o gateway do Azure denominado gatewayName no resourceGroupName do grupo de recursos, recupera as rotas que estão sendo anunciadas para o primeiro par BGP na lista de pares BGP do gateway.</span><span class="sxs-lookup"><span data-stu-id="03064-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="03064-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03064-112">PARAMETERS</span></span>

### <span data-ttu-id="03064-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03064-113">-AsJob</span></span>
<span data-ttu-id="03064-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="03064-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03064-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03064-115">-DefaultProfile</span></span>
<span data-ttu-id="03064-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="03064-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03064-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="03064-117">-Peer</span></span>
<span data-ttu-id="03064-118">Endereço IP do par BGP.</span><span class="sxs-lookup"><span data-stu-id="03064-118">BGP peer's IP address.</span></span> <span data-ttu-id="03064-119">Esse deve ser um IP dentro do espaço de endereço acessível de dentro da rede virtual do Azure em que o gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="03064-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="03064-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03064-120">-ResourceGroupName</span></span>
<span data-ttu-id="03064-121">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="03064-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="03064-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="03064-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="03064-123">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="03064-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="03064-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03064-124">CommonParameters</span></span>
<span data-ttu-id="03064-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03064-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03064-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03064-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03064-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03064-127">INPUTS</span></span>

### <span data-ttu-id="03064-128">System.String</span><span class="sxs-lookup"><span data-stu-id="03064-128">System.String</span></span>

## <span data-ttu-id="03064-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03064-129">OUTPUTS</span></span>

### <span data-ttu-id="03064-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="03064-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="03064-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="03064-131">NOTES</span></span>
<span data-ttu-id="03064-132">Esse comando só é aplicável aos gateways de rede virtual do Azure com conexões BGP habilitadas.</span><span class="sxs-lookup"><span data-stu-id="03064-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="03064-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03064-133">RELATED LINKS</span></span>
