---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428108"
---
# <span data-ttu-id="f9f4f-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="f9f4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f4f-103">Atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-103">Updates a virtual network.</span></span>

## <span data-ttu-id="f9f4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9f4f-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9f4f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f4f-106">O cmdlet **set-AzVirtualNetwork** atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="f9f4f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="f9f4f-108">1: cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="f9f4f-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="f9f4f-109">Este exemplo cria uma rede virtual chamada TestResourceGroup com duas sub-redes: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="f9f4f-110">Em seguida, ele remove a sub-rede backendSubnet da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f9f4f-111">O cmdlet Set-AzVirtualNetwork é usado para gravar o estado da rede virtual modificada no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="f9f4f-112">Quando o cmdlet Set-AzVirtualNetwork for executado, o backendSubnet será removido.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="f9f4f-113">OS</span><span class="sxs-lookup"><span data-stu-id="f9f4f-113">PARAMETERS</span></span>

### <span data-ttu-id="f9f4f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9f4f-114">-AsJob</span></span>
<span data-ttu-id="f9f4f-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f9f4f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f4f-116">-DefaultProfile</span></span>
<span data-ttu-id="f9f4f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9f4f-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-118">-VirtualNetwork</span></span>
<span data-ttu-id="f9f4f-119">Especifica um objeto de rede virtual que representa o estado para o qual a rede virtual deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9f4f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f4f-120">CommonParameters</span></span>
<span data-ttu-id="f9f4f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f4f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f4f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f4f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f4f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9f4f-123">INPUTS</span></span>

### <span data-ttu-id="f9f4f-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f9f4f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9f4f-125">OUTPUTS</span></span>

### <span data-ttu-id="f9f4f-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f9f4f-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9f4f-127">NOTES</span></span>

## <span data-ttu-id="f9f4f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9f4f-128">RELATED LINKS</span></span>

[<span data-ttu-id="f9f4f-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f9f4f-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f9f4f-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f9f4f-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f4f-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


