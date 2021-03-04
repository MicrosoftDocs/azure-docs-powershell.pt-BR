---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 1c5a5bc119c481c47c865ca72896b832f3a82b2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891332"
---
# <span data-ttu-id="a3139-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="a3139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3139-102">SYNOPSIS</span></span>
<span data-ttu-id="a3139-103">Atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a3139-103">Updates a virtual network.</span></span>

## <span data-ttu-id="a3139-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3139-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3139-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3139-105">DESCRIPTION</span></span>
<span data-ttu-id="a3139-106">O cmdlet **Set-AzVirtualNetwork** atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a3139-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="a3139-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3139-107">EXAMPLES</span></span>

### <span data-ttu-id="a3139-108">1: cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="a3139-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="a3139-109">Este exemplo cria uma rede virtual chamada TestResourceGroup com duas sub-redes: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="a3139-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="a3139-110">Em seguida, ele remove a sub-rede backendSubnet da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a3139-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a3139-111">O Set-AzVirtualNetwork cmdlet é usado para gravar o estado de rede virtual modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="a3139-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="a3139-112">Quando o cmdlet Set-AzVirtualNetwork é executado, o backendSubnet é removido.</span><span class="sxs-lookup"><span data-stu-id="a3139-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="a3139-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3139-113">PARAMETERS</span></span>

### <span data-ttu-id="a3139-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3139-114">-AsJob</span></span>
<span data-ttu-id="a3139-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3139-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3139-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3139-116">-DefaultProfile</span></span>
<span data-ttu-id="a3139-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a3139-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3139-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-118">-VirtualNetwork</span></span>
<span data-ttu-id="a3139-119">Especifica um objeto de rede virtual que representa o estado ao qual a rede virtual deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="a3139-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="a3139-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3139-120">CommonParameters</span></span>
<span data-ttu-id="a3139-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3139-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3139-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3139-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3139-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3139-123">INPUTS</span></span>

### <span data-ttu-id="a3139-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a3139-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3139-125">OUTPUTS</span></span>

### <span data-ttu-id="a3139-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a3139-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3139-127">NOTES</span></span>

## <span data-ttu-id="a3139-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3139-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3139-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="a3139-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="a3139-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="a3139-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3139-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


