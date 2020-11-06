---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430173"
---
# <span data-ttu-id="b0797-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b0797-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b0797-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0797-102">SYNOPSIS</span></span>
<span data-ttu-id="b0797-103">Obtém uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b0797-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0797-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0797-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0797-105">DESCRIPTION</span></span>
<span data-ttu-id="b0797-106">O cmdlet **Get-AzureRmLoadBalancerBackendAddressPoolConfig** Obtém um único pool de endereços back-end ou uma lista de pools de endereços back-end dentro de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b0797-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="b0797-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0797-107">EXAMPLES</span></span>

### <span data-ttu-id="b0797-108">Exemplo 1: obter o pool de endereços back-end</span><span class="sxs-lookup"><span data-stu-id="b0797-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b0797-109">O primeiro comando obtém um balanceador de carga existente chamado MyLoadBalancer no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b0797-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="b0797-110">O segundo comando obtém a configuração de pool de endereços back-end associada chamada BackendAddressPool02 para o balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b0797-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b0797-111">OS</span><span class="sxs-lookup"><span data-stu-id="b0797-111">PARAMETERS</span></span>

### <span data-ttu-id="b0797-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0797-112">-DefaultProfile</span></span>
<span data-ttu-id="b0797-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0797-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0797-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b0797-114">-LoadBalancer</span></span>
<span data-ttu-id="b0797-115">Especifica o balanceador de carga que está associado ao pool de endereços back-end para obter.</span><span class="sxs-lookup"><span data-stu-id="b0797-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0797-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0797-116">-Name</span></span>
<span data-ttu-id="b0797-117">Especifica o nome do balanceador de carga que contém o pool de endereços de back-end a obter.</span><span class="sxs-lookup"><span data-stu-id="b0797-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0797-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0797-118">CommonParameters</span></span>
<span data-ttu-id="b0797-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0797-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0797-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0797-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0797-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0797-121">INPUTS</span></span>

### <span data-ttu-id="b0797-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0797-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="b0797-123">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0797-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="b0797-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0797-124">OUTPUTS</span></span>

### <span data-ttu-id="b0797-125">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b0797-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b0797-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0797-126">NOTES</span></span>

## <span data-ttu-id="b0797-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0797-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0797-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b0797-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b0797-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b0797-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b0797-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b0797-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b0797-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b0797-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)

