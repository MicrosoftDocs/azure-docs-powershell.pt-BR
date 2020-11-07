---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775640"
---
# <span data-ttu-id="f4653-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f4653-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f4653-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4653-102">SYNOPSIS</span></span>
<span data-ttu-id="f4653-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f4653-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="f4653-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4653-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4653-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4653-105">DESCRIPTION</span></span>
<span data-ttu-id="f4653-106">O cmdlet **Add-AzLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4653-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="f4653-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4653-107">EXAMPLES</span></span>

### <span data-ttu-id="f4653-108">Exemplo 1 adicionar uma configuração de pool de endereços de back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f4653-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="f4653-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 a MyLoadBalancer e, em seguida, usa o cmdlet **set-AzLoadBalancer** para atualizar MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f4653-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="f4653-110">OS</span><span class="sxs-lookup"><span data-stu-id="f4653-110">PARAMETERS</span></span>

### <span data-ttu-id="f4653-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4653-111">-DefaultProfile</span></span>
<span data-ttu-id="f4653-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4653-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4653-113">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f4653-113">-LoadBalancer</span></span>
<span data-ttu-id="f4653-114">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="f4653-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="f4653-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4653-115">-Name</span></span>
<span data-ttu-id="f4653-116">Especifica o nome da configuração do pool de endereços back-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="f4653-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="f4653-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4653-117">CommonParameters</span></span>
<span data-ttu-id="f4653-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4653-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4653-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4653-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4653-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4653-120">INPUTS</span></span>

### <span data-ttu-id="f4653-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4653-121">PSLoadBalancer</span></span>
<span data-ttu-id="f4653-122">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f4653-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f4653-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4653-123">OUTPUTS</span></span>

### <span data-ttu-id="f4653-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4653-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f4653-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4653-125">NOTES</span></span>

## <span data-ttu-id="f4653-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4653-126">RELATED LINKS</span></span>

[<span data-ttu-id="f4653-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4653-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f4653-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f4653-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f4653-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f4653-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f4653-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f4653-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f4653-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f4653-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


