---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440111"
---
# <span data-ttu-id="86861-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="86861-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="86861-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86861-102">SYNOPSIS</span></span>
<span data-ttu-id="86861-103">Remove o site padrão de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="86861-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86861-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86861-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86861-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86861-105">DESCRIPTION</span></span>
<span data-ttu-id="86861-106">O cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** remove o site padrão de encapsulamento forçado de um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="86861-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="86861-107">O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="86861-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="86861-108">O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="86861-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="86861-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="86861-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="86861-110">Se fizer isso, você precisará usar o Set-AzureRmVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="86861-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="86861-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86861-111">EXAMPLES</span></span>

### <span data-ttu-id="86861-112">Exemplo 1: remover o site padrão atribuído a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="86861-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="86861-113">Este exemplo remove o site padrão atribuído atualmente a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="86861-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="86861-114">O primeiro comando usa **Get-AzureRmVirtualNetworkGateway** para criar uma referência de objeto para o gateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="86861-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="86861-115">Em seguida, o segundo comando usa **Remove-AzureRmVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.</span><span class="sxs-lookup"><span data-stu-id="86861-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="86861-116">OS</span><span class="sxs-lookup"><span data-stu-id="86861-116">PARAMETERS</span></span>

### <span data-ttu-id="86861-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86861-117">-DefaultProfile</span></span>
<span data-ttu-id="86861-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86861-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86861-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86861-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="86861-120">Especifica uma referência de objeto para o gateway de rede virtual que contém o site padrão a ser removido.</span><span class="sxs-lookup"><span data-stu-id="86861-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="86861-121">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="86861-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="86861-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86861-122">CommonParameters</span></span>
<span data-ttu-id="86861-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86861-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86861-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86861-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86861-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86861-125">INPUTS</span></span>

###  
<span data-ttu-id="86861-126">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="86861-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="86861-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86861-127">OUTPUTS</span></span>

###  
<span data-ttu-id="86861-128">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="86861-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="86861-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86861-129">NOTES</span></span>

## <span data-ttu-id="86861-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86861-130">RELATED LINKS</span></span>

[<span data-ttu-id="86861-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86861-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="86861-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="86861-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


