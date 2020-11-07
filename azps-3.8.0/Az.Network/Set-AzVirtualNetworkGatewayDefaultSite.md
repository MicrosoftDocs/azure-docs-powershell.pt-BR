---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940659"
---
# <span data-ttu-id="da73e-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="da73e-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="da73e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da73e-102">SYNOPSIS</span></span>
<span data-ttu-id="da73e-103">Define o site padrão para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="da73e-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="da73e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da73e-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da73e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da73e-105">DESCRIPTION</span></span>
<span data-ttu-id="da73e-106">O cmdlet **set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de encapsulamento forçado a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="da73e-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="da73e-107">O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="da73e-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="da73e-108">O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="da73e-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="da73e-109">**Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="da73e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da73e-110">EXAMPLES</span></span>

### <span data-ttu-id="da73e-111">Exemplo 1: atribuir um site padrão a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="da73e-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="da73e-112">Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="da73e-113">O primeiro comando cria uma referência de objeto para um gateway local chamado ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="da73e-114">Essa referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão.</span><span class="sxs-lookup"><span data-stu-id="da73e-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="da73e-115">Em seguida, o segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="da73e-116">O terceiro comando usa o cmdlet **set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="da73e-117">OS</span><span class="sxs-lookup"><span data-stu-id="da73e-117">PARAMETERS</span></span>

### <span data-ttu-id="da73e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da73e-118">-DefaultProfile</span></span>
<span data-ttu-id="da73e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da73e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da73e-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="da73e-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="da73e-121">Especifica uma referência de objeto para o gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="da73e-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="da73e-122">Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto para um gateway local.</span><span class="sxs-lookup"><span data-stu-id="da73e-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="da73e-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="da73e-124">Especifica uma referência de objeto para o gateway de rede virtual em que o site padrão será atribuído.</span><span class="sxs-lookup"><span data-stu-id="da73e-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="da73e-125">Você pode criar uma referência de objeto para um gateway de rede virtual usando **Get-AzVirtualNetworkGateway** e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="da73e-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="da73e-126">A variável $VirtualGateway pode ser usada como o valor do parâmetro para o parâmetro *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="da73e-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="da73e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da73e-127">CommonParameters</span></span>
<span data-ttu-id="da73e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da73e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da73e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da73e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da73e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da73e-130">INPUTS</span></span>

### <span data-ttu-id="da73e-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="da73e-132">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="da73e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da73e-133">OUTPUTS</span></span>

### <span data-ttu-id="da73e-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="da73e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da73e-135">NOTES</span></span>

## <span data-ttu-id="da73e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da73e-136">RELATED LINKS</span></span>

[<span data-ttu-id="da73e-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="da73e-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="da73e-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="da73e-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="da73e-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


