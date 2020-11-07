---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786429"
---
# <span data-ttu-id="ed414-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ed414-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="ed414-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed414-102">SYNOPSIS</span></span>
<span data-ttu-id="ed414-103">Remove uma configuração de pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ed414-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed414-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed414-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed414-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed414-105">DESCRIPTION</span></span>
<span data-ttu-id="ed414-106">O cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ed414-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="ed414-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed414-107">EXAMPLES</span></span>

### <span data-ttu-id="ed414-108">Exemplo 1: remover uma configuração de pool de endereços de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ed414-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="ed414-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer e o passa para **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ed414-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="ed414-110">Por fim, o cmdlet Set-AzureRmLoadBalancer atualiza MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ed414-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="ed414-111">Observe que uma configuração de pool de endereços back-end deve existir antes que você possa excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="ed414-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="ed414-112">OS</span><span class="sxs-lookup"><span data-stu-id="ed414-112">PARAMETERS</span></span>

### <span data-ttu-id="ed414-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed414-113">-DefaultProfile</span></span>
<span data-ttu-id="ed414-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed414-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed414-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="ed414-115">-LoadBalancer</span></span>
<span data-ttu-id="ed414-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ed414-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="ed414-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed414-117">-Name</span></span>
<span data-ttu-id="ed414-118">Especifica o nome do pool de endereços back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ed414-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed414-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed414-119">CommonParameters</span></span>
<span data-ttu-id="ed414-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed414-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed414-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed414-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed414-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed414-122">INPUTS</span></span>

### <span data-ttu-id="ed414-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed414-123">PSLoadBalancer</span></span>
<span data-ttu-id="ed414-124">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ed414-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ed414-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed414-125">OUTPUTS</span></span>

### <span data-ttu-id="ed414-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed414-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ed414-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed414-127">NOTES</span></span>

## <span data-ttu-id="ed414-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed414-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed414-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ed414-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ed414-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ed414-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ed414-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ed414-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ed414-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ed414-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


