---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9516d132f2c6b26c162dcbb8abc742e69dccfc14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772247"
---
# <span data-ttu-id="f233e-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f233e-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="f233e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f233e-102">SYNOPSIS</span></span>
<span data-ttu-id="f233e-103">Remove o site padrão de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f233e-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="f233e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f233e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f233e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f233e-105">DESCRIPTION</span></span>
<span data-ttu-id="f233e-106">O cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão de encapsulamento forçado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f233e-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="f233e-107">O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="f233e-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="f233e-108">O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="f233e-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="f233e-109">**Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="f233e-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="f233e-110">Se fizer isso, você precisará usar o Set-AzVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="f233e-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="f233e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f233e-111">EXAMPLES</span></span>

### <span data-ttu-id="f233e-112">Exemplo 1: remover o site padrão atribuído a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f233e-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="f233e-113">Este exemplo remove o site padrão atribuído atualmente a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f233e-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f233e-114">O primeiro comando usa **Get-AzVirtualNetworkGateway** para criar uma referência de objeto para o gateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f233e-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="f233e-115">Em seguida, o segundo comando usa **Remove-AzVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.</span><span class="sxs-lookup"><span data-stu-id="f233e-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="f233e-116">OS</span><span class="sxs-lookup"><span data-stu-id="f233e-116">PARAMETERS</span></span>

### <span data-ttu-id="f233e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f233e-117">-DefaultProfile</span></span>
<span data-ttu-id="f233e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f233e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f233e-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f233e-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f233e-120">Especifica uma referência de objeto para o gateway de rede virtual que contém o site padrão a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f233e-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="f233e-121">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="f233e-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="f233e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f233e-122">CommonParameters</span></span>
<span data-ttu-id="f233e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f233e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f233e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f233e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f233e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f233e-125">INPUTS</span></span>

### <span data-ttu-id="f233e-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f233e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f233e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f233e-127">OUTPUTS</span></span>

### <span data-ttu-id="f233e-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f233e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f233e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f233e-129">NOTES</span></span>

## <span data-ttu-id="f233e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f233e-130">RELATED LINKS</span></span>

[<span data-ttu-id="f233e-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f233e-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f233e-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f233e-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)

