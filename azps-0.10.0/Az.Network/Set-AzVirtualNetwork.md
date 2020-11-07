---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776505"
---
# <span data-ttu-id="9d2d7-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="9d2d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2d7-103">Define o estado da meta para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="9d2d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d2d7-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d2d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d2d7-105">DESCRIPTION</span></span>
<span data-ttu-id="9d2d7-106">O cmdlet **set-AzVirtualNetwork** define o estado da meta para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="9d2d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-107">EXAMPLES</span></span>

### <span data-ttu-id="9d2d7-108">1: cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="9d2d7-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9d2d7-109">Este exemplo cria uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="9d2d7-110">Em seguida, ele remove uma sub-rede da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9d2d7-111">O cmdlet Set-AzVirtualNetwork é usado para gravar o estado da rede virtual modificada no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="9d2d7-112">OS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-112">PARAMETERS</span></span>

### <span data-ttu-id="9d2d7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d2d7-113">-AsJob</span></span>
<span data-ttu-id="9d2d7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9d2d7-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d2d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2d7-115">-DefaultProfile</span></span>
<span data-ttu-id="9d2d7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d2d7-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-117">-VirtualNetwork</span></span>
<span data-ttu-id="9d2d7-118">Especifica um objeto **VirtualNetwork** que representa o estado da meta.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d2d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2d7-119">CommonParameters</span></span>
<span data-ttu-id="9d2d7-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2d7-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2d7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2d7-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d2d7-122">INPUTS</span></span>

### <span data-ttu-id="9d2d7-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-123">PSVirtualNetwork</span></span>
<span data-ttu-id="9d2d7-124">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="9d2d7-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="9d2d7-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d2d7-125">OUTPUTS</span></span>

### <span data-ttu-id="9d2d7-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9d2d7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d2d7-127">NOTES</span></span>

## <span data-ttu-id="9d2d7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d2d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d2d7-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9d2d7-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9d2d7-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9d2d7-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9d2d7-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

