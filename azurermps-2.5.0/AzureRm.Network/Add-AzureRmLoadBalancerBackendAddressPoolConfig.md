---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 3538a74b2ac638270d5487039faf9f8268d6efa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785732"
---
# <span data-ttu-id="8754b-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8754b-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8754b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8754b-102">SYNOPSIS</span></span>
<span data-ttu-id="8754b-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8754b-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8754b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8754b-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8754b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8754b-105">DESCRIPTION</span></span>
<span data-ttu-id="8754b-106">O cmdlet **Add-AzureRmLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="8754b-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="8754b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8754b-107">EXAMPLES</span></span>

### <span data-ttu-id="8754b-108">Exemplo 1 adicionar uma configuração de pool de endereços de back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="8754b-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="8754b-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 a MyLoadBalancer e, em seguida, usa o cmdlet **set-AzureRmLoadBalancer** para atualizar MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="8754b-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="8754b-110">OS</span><span class="sxs-lookup"><span data-stu-id="8754b-110">PARAMETERS</span></span>

### <span data-ttu-id="8754b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8754b-111">-DefaultProfile</span></span>
<span data-ttu-id="8754b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8754b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8754b-113">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="8754b-113">-LoadBalancer</span></span>
<span data-ttu-id="8754b-114">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="8754b-114">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8754b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8754b-115">-Name</span></span>
<span data-ttu-id="8754b-116">Especifica o nome da configuração do pool de endereços back-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="8754b-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8754b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8754b-117">CommonParameters</span></span>
<span data-ttu-id="8754b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8754b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8754b-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8754b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8754b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8754b-120">INPUTS</span></span>

### <span data-ttu-id="8754b-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8754b-121">PSLoadBalancer</span></span>
<span data-ttu-id="8754b-122">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8754b-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8754b-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8754b-123">OUTPUTS</span></span>

### <span data-ttu-id="8754b-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8754b-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8754b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8754b-125">NOTES</span></span>

## <span data-ttu-id="8754b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8754b-126">RELATED LINKS</span></span>

[<span data-ttu-id="8754b-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8754b-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="8754b-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8754b-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="8754b-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8754b-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8754b-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8754b-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8754b-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8754b-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


