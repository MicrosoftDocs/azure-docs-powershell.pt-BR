---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440322"
---
# <span data-ttu-id="d49ed-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d49ed-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="d49ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d49ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d49ed-103">Redimensiona um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="d49ed-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d49ed-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d49ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d49ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d49ed-106">O cmdlet **Resize-AzureRmVirtualNetworkGateway** permite que você altere a SKU (unidade de manutenção de estoque) para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d49ed-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="d49ed-107">Os SKUs determinam os recursos de um gateway, incluindo itens como throughput e o número máximo de túneis de IP permitidos.</span><span class="sxs-lookup"><span data-stu-id="d49ed-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="d49ed-108">O Azure é compatível com os SKUs básico, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (às vezes chamado de SKUs pequeno, médio e grande).</span><span class="sxs-lookup"><span data-stu-id="d49ed-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="d49ed-109">Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="d49ed-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="d49ed-110">Lembre-se de que os SKUs são diferentes em preços e recursos.</span><span class="sxs-lookup"><span data-stu-id="d49ed-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="d49ed-111">Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="d49ed-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="d49ed-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d49ed-112">EXAMPLES</span></span>

### <span data-ttu-id="d49ed-113">Exemplo 1: alterar o tamanho de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d49ed-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="d49ed-114">Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="d49ed-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="d49ed-115">O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d49ed-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="d49ed-116">Em seguida, o segundo comando usa o cmdlet **Resize-AzureRmVirtualNetworkGateway** para definir a propriedade *GatewaySku* como Basic.</span><span class="sxs-lookup"><span data-stu-id="d49ed-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="d49ed-117">OS</span><span class="sxs-lookup"><span data-stu-id="d49ed-117">PARAMETERS</span></span>

### <span data-ttu-id="d49ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49ed-118">-DefaultProfile</span></span>
<span data-ttu-id="d49ed-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d49ed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d49ed-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d49ed-120">-GatewaySku</span></span>
<span data-ttu-id="d49ed-121">Especifica o novo tipo de SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="d49ed-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="d49ed-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d49ed-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d49ed-123">Basic</span><span class="sxs-lookup"><span data-stu-id="d49ed-123">Basic</span></span>
- <span data-ttu-id="d49ed-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="d49ed-124">Standard</span></span>
- <span data-ttu-id="d49ed-125">Alto desempenho</span><span class="sxs-lookup"><span data-stu-id="d49ed-125">High Performance</span></span>
- <span data-ttu-id="d49ed-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d49ed-126">VpnGw1</span></span>
- <span data-ttu-id="d49ed-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d49ed-127">VpnGw2</span></span>
- <span data-ttu-id="d49ed-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d49ed-128">VpnGw3</span></span>
- <span data-ttu-id="d49ed-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="d49ed-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="d49ed-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="d49ed-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-132">ErGw1AZ</span></span> 
- <span data-ttu-id="d49ed-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-133">ErGw2AZ</span></span> 
- <span data-ttu-id="d49ed-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d49ed-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ed-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d49ed-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d49ed-136">Especifica uma referência de objeto ao gateway de rede virtual a ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="d49ed-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="d49ed-137">Você pode criar essa referência de objeto usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="d49ed-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="d49ed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49ed-138">CommonParameters</span></span>
<span data-ttu-id="d49ed-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49ed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49ed-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49ed-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49ed-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d49ed-141">INPUTS</span></span>

### <span data-ttu-id="d49ed-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d49ed-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d49ed-143">Parâmetros: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d49ed-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="d49ed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d49ed-144">System.String</span></span>

## <span data-ttu-id="d49ed-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d49ed-145">OUTPUTS</span></span>

### <span data-ttu-id="d49ed-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d49ed-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d49ed-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d49ed-147">NOTES</span></span>
<span data-ttu-id="d49ed-148">Não é possível redimensionar os SKUs Basic/Standard/HighPerformance para os novos SKUs VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="d49ed-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="d49ed-149">Redimensionar ainda não é permitido de/para VpnGw1AZ/VpnGw2AZ/VpnGw3AZ ou ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="d49ed-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="d49ed-150">Só é permitido o redimensionamento dentro da série de SKU ', pois VpnGw1AZ pode ser redimensionado para/de VpnGw2AZ/VpnGw3AZ e ErGw1AZ pode ser redimensionado para/de ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="d49ed-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="d49ed-151">Consulte https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="d49ed-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="d49ed-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d49ed-152">RELATED LINKS</span></span>

[<span data-ttu-id="d49ed-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="d49ed-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="d49ed-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d49ed-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d49ed-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="d49ed-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)

