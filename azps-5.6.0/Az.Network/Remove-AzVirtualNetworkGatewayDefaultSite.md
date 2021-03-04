---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892402"
---
# <span data-ttu-id="9785c-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9785c-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="9785c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9785c-102">SYNOPSIS</span></span>
<span data-ttu-id="9785c-103">Remove o site padrão de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9785c-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="9785c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9785c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9785c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9785c-105">DESCRIPTION</span></span>
<span data-ttu-id="9785c-106">O cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão de tunelamento forçado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9785c-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="9785c-107">O túnel forçado fornece uma maneira de redirecionar o tráfego vinculado à Internet de máquinas virtuais do Azure para sua rede local; isso permite inspecionar e auditar o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="9785c-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="9785c-108">O tunelamento forçado é realizado usando um túnel vpn (rede virtual privada). esse túnel requer um site padrão, um gateway local onde todo o tráfego vinculado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="9785c-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="9785c-109">**Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="9785c-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="9785c-110">Se você fizer isso, precisará usar o Set-AzVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="9785c-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="9785c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9785c-111">EXAMPLES</span></span>

### <span data-ttu-id="9785c-112">Exemplo 1: Remover o site padrão atribuído a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9785c-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="9785c-113">Este exemplo remove o site padrão atualmente atribuído a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9785c-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="9785c-114">O primeiro comando usa **Get-AzVirtualNetworkGateway** para criar uma referência de objeto ao gateway; essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9785c-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="9785c-115">O segundo comando usa **Remove-AzVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.</span><span class="sxs-lookup"><span data-stu-id="9785c-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="9785c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9785c-116">PARAMETERS</span></span>

### <span data-ttu-id="9785c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9785c-117">-DefaultProfile</span></span>
<span data-ttu-id="9785c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9785c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9785c-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9785c-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9785c-120">Especifica uma referência de objeto ao gateway de rede virtual que contém o site padrão a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9785c-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="9785c-121">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="9785c-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="9785c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9785c-122">CommonParameters</span></span>
<span data-ttu-id="9785c-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9785c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9785c-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9785c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9785c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9785c-125">INPUTS</span></span>

### <span data-ttu-id="9785c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9785c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9785c-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9785c-127">OUTPUTS</span></span>

### <span data-ttu-id="9785c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9785c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9785c-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="9785c-129">NOTES</span></span>

## <span data-ttu-id="9785c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9785c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9785c-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9785c-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9785c-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9785c-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


