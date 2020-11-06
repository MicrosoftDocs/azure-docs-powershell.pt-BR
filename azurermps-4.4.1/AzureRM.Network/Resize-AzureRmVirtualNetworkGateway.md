---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611089"
---
# <span data-ttu-id="c7604-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7604-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="c7604-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7604-102">SYNOPSIS</span></span>
<span data-ttu-id="c7604-103">Redimensiona um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="c7604-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7604-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7604-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7604-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7604-105">DESCRIPTION</span></span>
<span data-ttu-id="c7604-106">O cmdlet **Resize-AzureRmVirtualNetworkGateway** permite que você altere a SKU (unidade de manutenção de estoque) para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c7604-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="c7604-107">Os SKUs determinam os recursos de um gateway, incluindo itens como throughput e o número máximo de túneis de IP permitidos.</span><span class="sxs-lookup"><span data-stu-id="c7604-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="c7604-108">O Azure é compatível com os SKUs Basic, Standard, High-Performance, VpnGw1, VpnGw2 e VpnGw3 (às vezes chamado de SKUs pequenos, médios e grandes).</span><span class="sxs-lookup"><span data-stu-id="c7604-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="c7604-109">Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="c7604-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="c7604-110">Lembre-se de que os SKUs são diferentes em preços e recursos.</span><span class="sxs-lookup"><span data-stu-id="c7604-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="c7604-111">Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="c7604-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="c7604-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7604-112">EXAMPLES</span></span>

### <span data-ttu-id="c7604-113">Exemplo 1: alterar o tamanho de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c7604-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="c7604-114">Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="c7604-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="c7604-115">O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7604-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="c7604-116">Em seguida, o segundo comando usa o cmdlet **Resize-AzureRmVirtualNetworkGateway** para definir a propriedade *GatewaySku* como Basic.</span><span class="sxs-lookup"><span data-stu-id="c7604-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="c7604-117">OS</span><span class="sxs-lookup"><span data-stu-id="c7604-117">PARAMETERS</span></span>

### <span data-ttu-id="c7604-118">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c7604-118">-GatewaySku</span></span>
<span data-ttu-id="c7604-119">Especifica o novo tipo de SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="c7604-119">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="c7604-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c7604-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7604-121">Basic</span><span class="sxs-lookup"><span data-stu-id="c7604-121">Basic</span></span>
- <span data-ttu-id="c7604-122">Oficial</span><span class="sxs-lookup"><span data-stu-id="c7604-122">Standard</span></span>
- <span data-ttu-id="c7604-123">Alto desempenho</span><span class="sxs-lookup"><span data-stu-id="c7604-123">High Performance</span></span>
- <span data-ttu-id="c7604-124">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c7604-124">VpnGw1</span></span>
- <span data-ttu-id="c7604-125">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c7604-125">VpnGw2</span></span>
- <span data-ttu-id="c7604-126">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c7604-126">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7604-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7604-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c7604-128">Especifica uma referência de objeto ao gateway de rede virtual a ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="c7604-128">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="c7604-129">Você pode criar essa referência de objeto usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="c7604-129">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7604-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7604-130">-DefaultProfile</span></span>
<span data-ttu-id="c7604-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7604-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7604-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7604-132">CommonParameters</span></span>
<span data-ttu-id="c7604-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7604-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7604-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7604-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7604-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7604-135">INPUTS</span></span>

###  
<span data-ttu-id="c7604-136">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c7604-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="c7604-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7604-137">OUTPUTS</span></span>

###  
<span data-ttu-id="c7604-138">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c7604-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="c7604-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7604-139">NOTES</span></span>
<span data-ttu-id="c7604-140">Não é possível redimensionar os SKUs Basic/Standard/HighPerformance para os novos SKUs VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="c7604-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="c7604-141">Consulte https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="c7604-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="c7604-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7604-142">RELATED LINKS</span></span>

[<span data-ttu-id="c7604-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="c7604-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="c7604-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7604-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c7604-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="c7604-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


