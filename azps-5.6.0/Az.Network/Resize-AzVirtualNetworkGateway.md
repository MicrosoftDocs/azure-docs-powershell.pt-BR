---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886155"
---
# <span data-ttu-id="515ec-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="515ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515ec-102">SYNOPSIS</span></span>
<span data-ttu-id="515ec-103">Resize um gateway de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="515ec-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="515ec-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="515ec-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="515ec-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="515ec-105">DESCRIPTION</span></span>
<span data-ttu-id="515ec-106">O cmdlet **Resize-AzVirtualNetworkGateway** permite que você altere a unidade de manutenção de estoque (SKU) para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="515ec-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="515ec-107">As SKUs determinam os recursos de um gateway, incluindo coisas como a produtividade e o número máximo de túneis IP permitidos.</span><span class="sxs-lookup"><span data-stu-id="515ec-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="515ec-108">O Azure oferece suporte a Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (às vezes chamados de Pequenas, Médias e Grandes SKUs).</span><span class="sxs-lookup"><span data-stu-id="515ec-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="515ec-109">Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="515ec-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="515ec-110">Lembre-se de que os SKUs diferem no preço, bem como nos recursos.</span><span class="sxs-lookup"><span data-stu-id="515ec-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="515ec-111">Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="515ec-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="515ec-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="515ec-112">EXAMPLES</span></span>

### <span data-ttu-id="515ec-113">Exemplo 1: Alterar o tamanho de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="515ec-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="515ec-114">Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="515ec-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="515ec-115">O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="515ec-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="515ec-116">O segundo comando usa o cmdlet **Resize-AzVirtualNetworkGateway** para definir a *propriedade GatewaySku* como Basic.</span><span class="sxs-lookup"><span data-stu-id="515ec-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="515ec-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="515ec-117">PARAMETERS</span></span>

### <span data-ttu-id="515ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515ec-118">-DefaultProfile</span></span>
<span data-ttu-id="515ec-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="515ec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515ec-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="515ec-120">-GatewaySku</span></span>
<span data-ttu-id="515ec-121">Especifica o novo tipo de SKU de gateway.</span><span class="sxs-lookup"><span data-stu-id="515ec-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="515ec-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="515ec-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="515ec-123">Básico</span><span class="sxs-lookup"><span data-stu-id="515ec-123">Basic</span></span>
- <span data-ttu-id="515ec-124">Standard</span><span class="sxs-lookup"><span data-stu-id="515ec-124">Standard</span></span>
- <span data-ttu-id="515ec-125">Alto desempenho</span><span class="sxs-lookup"><span data-stu-id="515ec-125">High Performance</span></span>
- <span data-ttu-id="515ec-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="515ec-126">VpnGw1</span></span>
- <span data-ttu-id="515ec-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="515ec-127">VpnGw2</span></span>
- <span data-ttu-id="515ec-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="515ec-128">VpnGw3</span></span>
- <span data-ttu-id="515ec-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="515ec-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="515ec-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="515ec-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-132">ErGw1AZ</span></span> 
- <span data-ttu-id="515ec-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-133">ErGw2AZ</span></span> 
- <span data-ttu-id="515ec-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="515ec-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="515ec-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="515ec-136">Especifica uma referência de objeto ao gateway de rede virtual a ser resized.</span><span class="sxs-lookup"><span data-stu-id="515ec-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="515ec-137">Você pode criar essa referência de objeto usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="515ec-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="515ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515ec-138">CommonParameters</span></span>
<span data-ttu-id="515ec-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515ec-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515ec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515ec-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="515ec-141">INPUTS</span></span>

### <span data-ttu-id="515ec-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="515ec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="515ec-143">System.String</span></span>

## <span data-ttu-id="515ec-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="515ec-144">OUTPUTS</span></span>

### <span data-ttu-id="515ec-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="515ec-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="515ec-146">NOTES</span></span>
<span data-ttu-id="515ec-147">Não é possível ressarci-lo de SKUs Basic/Standard/HighPerformance para as novas SKUs VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="515ec-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="515ec-148">O ressarte posterior não é permitido de/para VpnGw1AZ/VpnGw2AZ/VpnGw3AZ ou ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="515ec-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="515ec-149">O resize só é permitido dentro da 'série' SKU, por exemplo, o VpnGw1AZ pode ser resizado para/de VpnGw2AZ/VpnGw3AZ e ErGw1AZ pode ser resized para/de ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="515ec-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="515ec-150">Consulte https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways instruções.</span><span class="sxs-lookup"><span data-stu-id="515ec-150">See https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="515ec-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="515ec-151">RELATED LINKS</span></span>

[<span data-ttu-id="515ec-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="515ec-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="515ec-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="515ec-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="515ec-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="515ec-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="515ec-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="515ec-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="515ec-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="515ec-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
