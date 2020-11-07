---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775302"
---
# <span data-ttu-id="7b20c-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b20c-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="7b20c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b20c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b20c-103">Remove uma configuração de pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="7b20c-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="7b20c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b20c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b20c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b20c-105">DESCRIPTION</span></span>
<span data-ttu-id="7b20c-106">O cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="7b20c-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="7b20c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b20c-107">EXAMPLES</span></span>

### <span data-ttu-id="7b20c-108">Exemplo 1: remover uma configuração de pool de endereços de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="7b20c-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="7b20c-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer e o passa para **Remove-AzLoadBalancerBackendAddressPoolConfig** , que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="7b20c-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="7b20c-110">Por fim, o cmdlet Set-AzLoadBalancer atualiza MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="7b20c-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="7b20c-111">Observe que uma configuração de pool de endereços back-end deve existir antes que você possa excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="7b20c-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="7b20c-112">OS</span><span class="sxs-lookup"><span data-stu-id="7b20c-112">PARAMETERS</span></span>

### <span data-ttu-id="7b20c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b20c-113">-DefaultProfile</span></span>
<span data-ttu-id="7b20c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b20c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b20c-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="7b20c-115">-LoadBalancer</span></span>
<span data-ttu-id="7b20c-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7b20c-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="7b20c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b20c-117">-Name</span></span>
<span data-ttu-id="7b20c-118">Especifica o nome do pool de endereços back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="7b20c-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b20c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b20c-119">CommonParameters</span></span>
<span data-ttu-id="7b20c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b20c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b20c-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b20c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b20c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b20c-122">INPUTS</span></span>

### <span data-ttu-id="7b20c-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b20c-123">PSLoadBalancer</span></span>
<span data-ttu-id="7b20c-124">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7b20c-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7b20c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b20c-125">OUTPUTS</span></span>

### <span data-ttu-id="7b20c-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b20c-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7b20c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b20c-127">NOTES</span></span>

## <span data-ttu-id="7b20c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b20c-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b20c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b20c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7b20c-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b20c-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7b20c-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b20c-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7b20c-132">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b20c-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


