---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114616"
---
# <span data-ttu-id="4132f-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4132f-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="4132f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4132f-102">SYNOPSIS</span></span>
<span data-ttu-id="4132f-103">Define o site padrão para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4132f-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="4132f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4132f-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4132f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4132f-105">DESCRIPTION</span></span>
<span data-ttu-id="4132f-106">O cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de túnel forçado a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4132f-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="4132f-107">O túnel forçado fornece uma maneira de redirecionar o tráfego vinculado à Internet de máquinas virtuais do Azure para sua rede local; isso permite inspecionar e auditar o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="4132f-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="4132f-108">O túnel forçado é realizado usando um túnel de rede virtual privada (VPN); esse túnel requer um site padrão, um gateway local onde todo o tráfego vinculado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="4132f-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="4132f-109">**O Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="4132f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4132f-110">EXAMPLES</span></span>

### <span data-ttu-id="4132f-111">Exemplo 1: Atribuir um site padrão a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4132f-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="4132f-112">Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="4132f-113">O primeiro comando cria uma referência de objeto a um gateway local chamado ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="4132f-114">Essa referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão.</span><span class="sxs-lookup"><span data-stu-id="4132f-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="4132f-115">O segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="4132f-116">O terceiro comando usa o cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão à ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="4132f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4132f-117">PARAMETERS</span></span>

### <span data-ttu-id="4132f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4132f-118">-DefaultProfile</span></span>
<span data-ttu-id="4132f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4132f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4132f-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4132f-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="4132f-121">Especifica uma referência de objeto ao gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="4132f-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="4132f-122">Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto a um gateway local.</span><span class="sxs-lookup"><span data-stu-id="4132f-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="4132f-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="4132f-124">Especifica uma referência de objeto ao gateway de rede virtual onde o site padrão será atribuído.</span><span class="sxs-lookup"><span data-stu-id="4132f-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="4132f-125">Você pode criar uma referência de objeto a um gateway de rede virtual usando o **Get-AzVirtualNetworkGateway** e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="4132f-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="4132f-126">A variável $VirtualGateway pode ser usada como o valor de parâmetro para o parâmetro *VirtualNetworkGateway:*</span><span class="sxs-lookup"><span data-stu-id="4132f-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="4132f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4132f-127">CommonParameters</span></span>
<span data-ttu-id="4132f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4132f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4132f-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4132f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4132f-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="4132f-130">INPUTS</span></span>

### <span data-ttu-id="4132f-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4132f-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="4132f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="4132f-133">OUTPUTS</span></span>

### <span data-ttu-id="4132f-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4132f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="4132f-135">NOTES</span></span>

## <span data-ttu-id="4132f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4132f-136">RELATED LINKS</span></span>

[<span data-ttu-id="4132f-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="4132f-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4132f-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4132f-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4132f-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


