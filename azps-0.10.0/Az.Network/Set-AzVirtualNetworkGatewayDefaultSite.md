---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776506"
---
# <span data-ttu-id="52079-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="52079-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="52079-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52079-102">SYNOPSIS</span></span>
<span data-ttu-id="52079-103">Define o site padrão para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52079-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="52079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52079-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52079-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52079-105">DESCRIPTION</span></span>
<span data-ttu-id="52079-106">O cmdlet **set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de encapsulamento forçado a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52079-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="52079-107">O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="52079-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="52079-108">O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="52079-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="52079-109">**Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.</span><span class="sxs-lookup"><span data-stu-id="52079-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="52079-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52079-110">EXAMPLES</span></span>

### <span data-ttu-id="52079-111">Exemplo 1: atribuir um site padrão a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="52079-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="52079-112">Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="52079-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="52079-113">O primeiro comando cria uma referência de objeto para um gateway local chamado ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="52079-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="52079-114">Esta referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão</span><span class="sxs-lookup"><span data-stu-id="52079-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="52079-115">.</span><span class="sxs-lookup"><span data-stu-id="52079-115">.</span></span>
<span data-ttu-id="52079-116">Em seguida, o segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="52079-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="52079-117">O terceiro comando usa o cmdlet **set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="52079-117">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="52079-118">OS</span><span class="sxs-lookup"><span data-stu-id="52079-118">PARAMETERS</span></span>

### <span data-ttu-id="52079-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52079-119">-DefaultProfile</span></span>
<span data-ttu-id="52079-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52079-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52079-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="52079-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="52079-122">Especifica uma referência de objeto para o gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="52079-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="52079-123">Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto para um gateway local.</span><span class="sxs-lookup"><span data-stu-id="52079-123">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52079-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52079-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="52079-125">Especifica uma referência de objeto para o gateway de rede virtual em que o site padrão será atribuído.</span><span class="sxs-lookup"><span data-stu-id="52079-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="52079-126">Você pode criar uma referência de objeto para um gateway de rede virtual usando **Get-AzVirtualNetworkGateway** e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="52079-126">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="52079-127">A variável $VirtualGateway pode ser usada como o valor do parâmetro para o parâmetro *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="52079-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="52079-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52079-128">CommonParameters</span></span>
<span data-ttu-id="52079-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52079-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52079-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52079-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52079-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52079-131">INPUTS</span></span>

###  
<span data-ttu-id="52079-132">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="52079-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="52079-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52079-133">OUTPUTS</span></span>

###  
<span data-ttu-id="52079-134">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="52079-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="52079-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52079-135">NOTES</span></span>

## <span data-ttu-id="52079-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52079-136">RELATED LINKS</span></span>

[<span data-ttu-id="52079-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52079-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="52079-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52079-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="52079-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="52079-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


