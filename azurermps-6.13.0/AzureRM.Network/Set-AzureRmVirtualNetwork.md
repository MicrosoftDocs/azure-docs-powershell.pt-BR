---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429415"
---
# <span data-ttu-id="99ff7-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="99ff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="99ff7-103">Define o estado da meta para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="99ff7-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99ff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99ff7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99ff7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="99ff7-106">O cmdlet **set-AzureRmVirtualNetwork** define o estado da meta para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="99ff7-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="99ff7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="99ff7-108">1: cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="99ff7-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="99ff7-109">Este exemplo cria uma rede virtual chamada TestResourceGroup com duas sub-redes: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="99ff7-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="99ff7-110">Em seguida, ele remove a sub-rede backendSubnet da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="99ff7-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="99ff7-111">O cmdlet Set-AzureRmVirtualNetwork é usado para gravar o estado da rede virtual modificada no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="99ff7-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="99ff7-112">Quando o cmdlet Set-AzureRmVirtualNetwork for executado, o backendSubnet será removido.</span><span class="sxs-lookup"><span data-stu-id="99ff7-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="99ff7-113">OS</span><span class="sxs-lookup"><span data-stu-id="99ff7-113">PARAMETERS</span></span>

### <span data-ttu-id="99ff7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99ff7-114">-AsJob</span></span>
<span data-ttu-id="99ff7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="99ff7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99ff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ff7-116">-DefaultProfile</span></span>
<span data-ttu-id="99ff7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99ff7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ff7-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-118">-VirtualNetwork</span></span>
<span data-ttu-id="99ff7-119">Especifica um objeto **VirtualNetwork** que representa o estado da meta.</span><span class="sxs-lookup"><span data-stu-id="99ff7-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="99ff7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ff7-120">CommonParameters</span></span>
<span data-ttu-id="99ff7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ff7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ff7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ff7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ff7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99ff7-123">INPUTS</span></span>

### <span data-ttu-id="99ff7-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="99ff7-125">Parâmetros: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="99ff7-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="99ff7-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99ff7-126">OUTPUTS</span></span>

### <span data-ttu-id="99ff7-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="99ff7-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99ff7-128">NOTES</span></span>

## <span data-ttu-id="99ff7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ff7-129">RELATED LINKS</span></span>

[<span data-ttu-id="99ff7-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99ff7-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99ff7-132">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99ff7-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99ff7-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


