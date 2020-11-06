---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: ef5071ff0127c34d9ae8c41ea12e2465e83c98d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603359"
---
# <span data-ttu-id="b8613-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b8613-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b8613-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8613-102">SYNOPSIS</span></span>
<span data-ttu-id="b8613-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b8613-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8613-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8613-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8613-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8613-105">DESCRIPTION</span></span>
<span data-ttu-id="b8613-106">O cmdlet **Add-AzureRmLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8613-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="b8613-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8613-107">EXAMPLES</span></span>

### <span data-ttu-id="b8613-108">Exemplo 1 adicionar uma configuração de pool de endereços de back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="b8613-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b8613-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 a MyLoadBalancer e, em seguida, usa o cmdlet **set-AzureRmLoadBalancer** para atualizar MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="b8613-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="b8613-110">OS</span><span class="sxs-lookup"><span data-stu-id="b8613-110">PARAMETERS</span></span>

### <span data-ttu-id="b8613-111">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b8613-111">-LoadBalancer</span></span>
<span data-ttu-id="b8613-112">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="b8613-112">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8613-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8613-113">-Name</span></span>
<span data-ttu-id="b8613-114">Especifica o nome da configuração do pool de endereços back-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="b8613-114">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8613-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8613-115">-DefaultProfile</span></span>
<span data-ttu-id="b8613-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8613-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8613-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8613-117">CommonParameters</span></span>
<span data-ttu-id="b8613-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8613-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8613-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8613-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8613-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8613-120">INPUTS</span></span>

### <span data-ttu-id="b8613-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8613-121">PSLoadBalancer</span></span>
<span data-ttu-id="b8613-122">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b8613-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b8613-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8613-123">OUTPUTS</span></span>

### <span data-ttu-id="b8613-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8613-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b8613-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8613-125">NOTES</span></span>

## <span data-ttu-id="b8613-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8613-126">RELATED LINKS</span></span>

[<span data-ttu-id="b8613-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b8613-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b8613-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b8613-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="b8613-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b8613-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b8613-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b8613-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b8613-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b8613-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


