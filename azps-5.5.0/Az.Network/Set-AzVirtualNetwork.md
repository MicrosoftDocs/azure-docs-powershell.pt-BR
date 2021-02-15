---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 023d50aaf32d894722e2167737703d24776a1fd5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115051"
---
# <span data-ttu-id="7dc5d-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="7dc5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc5d-103">Atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-103">Updates a virtual network.</span></span>

## <span data-ttu-id="7dc5d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dc5d-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc5d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc5d-106">O cmdlet **Set-AzVirtualNetwork** atualiza uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="7dc5d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7dc5d-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc5d-108">1: Cria uma rede virtual e remove uma de suas sub-redes</span><span class="sxs-lookup"><span data-stu-id="7dc5d-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="7dc5d-109">Este exemplo cria uma rede virtual chamada TestResourceGroup com duas sub-redes: frontendSubnet e backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="7dc5d-110">Em seguida, remove a sub-rede backendSubnet da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7dc5d-111">O Set-AzVirtualNetwork cmdlet é usado para escrever o estado de rede virtual modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="7dc5d-112">Quando o cmdlet Set-AzVirtualNetwork é executado, a backendSubnet é removida.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="7dc5d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dc5d-113">PARAMETERS</span></span>

### <span data-ttu-id="7dc5d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dc5d-114">-AsJob</span></span>
<span data-ttu-id="7dc5d-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7dc5d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dc5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc5d-116">-DefaultProfile</span></span>
<span data-ttu-id="7dc5d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc5d-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-118">-VirtualNetwork</span></span>
<span data-ttu-id="7dc5d-119">Especifica um objeto de rede virtual que representa o estado ao qual a rede virtual deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="7dc5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc5d-120">CommonParameters</span></span>
<span data-ttu-id="7dc5d-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc5d-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc5d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc5d-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="7dc5d-123">INPUTS</span></span>

### <span data-ttu-id="7dc5d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7dc5d-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="7dc5d-125">OUTPUTS</span></span>

### <span data-ttu-id="7dc5d-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7dc5d-127">Notas</span><span class="sxs-lookup"><span data-stu-id="7dc5d-127">NOTES</span></span>

## <span data-ttu-id="7dc5d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dc5d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7dc5d-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7dc5d-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7dc5d-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7dc5d-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dc5d-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


