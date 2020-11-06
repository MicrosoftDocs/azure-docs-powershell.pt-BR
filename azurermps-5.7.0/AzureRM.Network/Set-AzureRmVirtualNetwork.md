---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 22ea0a6a28a24503413fa9b8958002616c03b884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428147"
---
# <span data-ttu-id="cdb0d-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="cdb0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb0d-103">Define o estado da meta para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdb0d-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdb0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdb0d-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb0d-106">O cmdlet **set-AzureRmVirtualNetwork** define o estado da meta para uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="cdb0d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdb0d-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb0d-108">1: cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="cdb0d-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="cdb0d-109">Este exemplo cria uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="cdb0d-110">Em seguida, ele remove uma sub-rede da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="cdb0d-111">O cmdlet Set-AzureRmVirtualNetwork é usado para gravar o estado da rede virtual modificada no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="cdb0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="cdb0d-112">PARAMETERS</span></span>

### <span data-ttu-id="cdb0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdb0d-113">-AsJob</span></span>
<span data-ttu-id="cdb0d-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cdb0d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdb0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb0d-115">-DefaultProfile</span></span>
<span data-ttu-id="cdb0d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb0d-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-117">-VirtualNetwork</span></span>
<span data-ttu-id="cdb0d-118">Especifica um objeto **VirtualNetwork** que representa o estado da meta.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="cdb0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb0d-119">CommonParameters</span></span>
<span data-ttu-id="cdb0d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb0d-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb0d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb0d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdb0d-122">INPUTS</span></span>

### <span data-ttu-id="cdb0d-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-123">PSVirtualNetwork</span></span>
<span data-ttu-id="cdb0d-124">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="cdb0d-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="cdb0d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdb0d-125">OUTPUTS</span></span>

### <span data-ttu-id="cdb0d-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cdb0d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdb0d-127">NOTES</span></span>

## <span data-ttu-id="cdb0d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdb0d-128">RELATED LINKS</span></span>

[<span data-ttu-id="cdb0d-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cdb0d-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cdb0d-131">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cdb0d-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cdb0d-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


