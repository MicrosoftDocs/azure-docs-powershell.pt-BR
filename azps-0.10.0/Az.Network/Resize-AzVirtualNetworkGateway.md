---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776584"
---
# <span data-ttu-id="dd115-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd115-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="dd115-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd115-102">SYNOPSIS</span></span>
<span data-ttu-id="dd115-103">Redimensiona um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="dd115-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="dd115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd115-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd115-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd115-105">DESCRIPTION</span></span>
<span data-ttu-id="dd115-106">O cmdlet **Resize-AzVirtualNetworkGateway** permite que você altere a SKU (unidade de manutenção de estoque) para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dd115-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="dd115-107">Os SKUs determinam os recursos de um gateway, incluindo itens como throughput e o número máximo de túneis de IP permitidos.</span><span class="sxs-lookup"><span data-stu-id="dd115-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="dd115-108">O Azure é compatível com os SKUs Basic, Standard, High-Performance, VpnGw1, VpnGw2 e VpnGw3 (às vezes chamado de SKUs pequenos, médios e grandes).</span><span class="sxs-lookup"><span data-stu-id="dd115-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="dd115-109">Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="dd115-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="dd115-110">Lembre-se de que os SKUs são diferentes em preços e recursos.</span><span class="sxs-lookup"><span data-stu-id="dd115-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="dd115-111">Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="dd115-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="dd115-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd115-112">EXAMPLES</span></span>

### <span data-ttu-id="dd115-113">Exemplo 1: alterar o tamanho de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dd115-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="dd115-114">Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="dd115-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="dd115-115">O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd115-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="dd115-116">Em seguida, o segundo comando usa o cmdlet **Resize-AzVirtualNetworkGateway** para definir a propriedade *GatewaySku* como Basic.</span><span class="sxs-lookup"><span data-stu-id="dd115-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="dd115-117">OS</span><span class="sxs-lookup"><span data-stu-id="dd115-117">PARAMETERS</span></span>

### <span data-ttu-id="dd115-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd115-118">-DefaultProfile</span></span>
<span data-ttu-id="dd115-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd115-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd115-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="dd115-120">-GatewaySku</span></span>
<span data-ttu-id="dd115-121">Especifica o novo tipo de SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="dd115-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="dd115-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dd115-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd115-123">Basic</span><span class="sxs-lookup"><span data-stu-id="dd115-123">Basic</span></span>
- <span data-ttu-id="dd115-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="dd115-124">Standard</span></span>
- <span data-ttu-id="dd115-125">Alto desempenho</span><span class="sxs-lookup"><span data-stu-id="dd115-125">High Performance</span></span>
- <span data-ttu-id="dd115-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="dd115-126">VpnGw1</span></span>
- <span data-ttu-id="dd115-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="dd115-127">VpnGw2</span></span>
- <span data-ttu-id="dd115-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="dd115-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd115-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd115-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="dd115-130">Especifica uma referência de objeto ao gateway de rede virtual a ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="dd115-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="dd115-131">Você pode criar essa referência de objeto usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="dd115-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd115-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd115-132">CommonParameters</span></span>
<span data-ttu-id="dd115-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd115-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd115-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd115-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd115-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd115-135">INPUTS</span></span>

###  
<span data-ttu-id="dd115-136">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="dd115-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="dd115-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd115-137">OUTPUTS</span></span>

###  
<span data-ttu-id="dd115-138">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="dd115-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="dd115-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd115-139">NOTES</span></span>
<span data-ttu-id="dd115-140">Não é possível redimensionar os SKUs Basic/Standard/HighPerformance para os novos SKUs VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="dd115-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="dd115-141">Consulte https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="dd115-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="dd115-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd115-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd115-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="dd115-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="dd115-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd115-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dd115-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="dd115-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)

