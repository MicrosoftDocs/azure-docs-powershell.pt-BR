---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888816"
---
# <span data-ttu-id="1a553-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1a553-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="1a553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a553-102">SYNOPSIS</span></span>
<span data-ttu-id="1a553-103">Define o site padrão para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1a553-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="1a553-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1a553-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a553-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1a553-105">DESCRIPTION</span></span>
<span data-ttu-id="1a553-106">O cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de tunelamento forçado a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1a553-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="1a553-107">O túnel forçado fornece uma maneira de redirecionar o tráfego vinculado à Internet de máquinas virtuais do Azure para sua rede local; isso permite inspecionar e auditar o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="1a553-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="1a553-108">O tunelamento forçado é realizado usando um túnel vpn (rede virtual privada). esse túnel requer um site padrão, um gateway local onde todo o tráfego vinculado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="1a553-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="1a553-109">**Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="1a553-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a553-110">EXAMPLES</span></span>

### <span data-ttu-id="1a553-111">Exemplo 1: Atribuir um site padrão a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1a553-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="1a553-112">Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="1a553-113">O primeiro comando cria uma referência de objeto a um gateway local chamado ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="1a553-114">Essa referência de objeto armazenada na variável denominada $LocalGateway representa o gateway a ser configurado como o site padrão .</span><span class="sxs-lookup"><span data-stu-id="1a553-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="1a553-115">O segundo comando cria uma referência de objeto ao gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="1a553-116">O terceiro comando usa o cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="1a553-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1a553-117">PARAMETERS</span></span>

### <span data-ttu-id="1a553-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a553-118">-DefaultProfile</span></span>
<span data-ttu-id="1a553-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1a553-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a553-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1a553-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="1a553-121">Especifica uma referência de objeto ao gateway de rede local a ser atribuído como o site padrão da rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="1a553-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="1a553-122">Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto a um gateway local.</span><span class="sxs-lookup"><span data-stu-id="1a553-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a553-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1a553-124">Especifica uma referência de objeto ao gateway de rede virtual onde o site padrão será atribuído.</span><span class="sxs-lookup"><span data-stu-id="1a553-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="1a553-125">Você pode criar uma referência de objeto a um gateway de rede virtual usando **o Get-AzVirtualNetworkGateway** e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="1a553-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="1a553-126">A variável $VirtualGateway pode ser usada como o valor de parâmetro para o *parâmetro VirtualNetworkGateway:*</span><span class="sxs-lookup"><span data-stu-id="1a553-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="1a553-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a553-127">CommonParameters</span></span>
<span data-ttu-id="1a553-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a553-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a553-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a553-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a553-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a553-130">INPUTS</span></span>

### <span data-ttu-id="1a553-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1a553-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1a553-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1a553-133">OUTPUTS</span></span>

### <span data-ttu-id="1a553-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1a553-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="1a553-135">NOTES</span></span>

## <span data-ttu-id="1a553-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a553-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a553-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="1a553-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a553-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1a553-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1a553-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


