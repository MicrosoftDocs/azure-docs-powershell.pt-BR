---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 0cc210563046a0ff8ee0554eb479e5eb822157fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610293"
---
# <span data-ttu-id="d652a-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d652a-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="d652a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d652a-102">SYNOPSIS</span></span>
<span data-ttu-id="d652a-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d652a-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d652a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d652a-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d652a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d652a-105">DESCRIPTION</span></span>
<span data-ttu-id="d652a-106">O cmdlet **Add-AzureRmLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="d652a-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="d652a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d652a-107">EXAMPLES</span></span>

### <span data-ttu-id="d652a-108">Exemplo 1 adicionar uma configuração de pool de endereços de back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d652a-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d652a-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 a MyLoadBalancer e, em seguida, usa o cmdlet **set-AzureRmLoadBalancer** para atualizar MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d652a-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="d652a-110">OS</span><span class="sxs-lookup"><span data-stu-id="d652a-110">PARAMETERS</span></span>

### <span data-ttu-id="d652a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d652a-111">-DefaultProfile</span></span>
<span data-ttu-id="d652a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d652a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d652a-113">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="d652a-113">-LoadBalancer</span></span>
<span data-ttu-id="d652a-114">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="d652a-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="d652a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d652a-115">-Name</span></span>
<span data-ttu-id="d652a-116">Especifica o nome da configuração do pool de endereços back-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="d652a-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="d652a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d652a-117">-Confirm</span></span>
<span data-ttu-id="d652a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d652a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d652a-119">-WhatIf</span></span>
<span data-ttu-id="d652a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d652a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d652a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d652a-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d652a-122">CommonParameters</span></span>
<span data-ttu-id="d652a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d652a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d652a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d652a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d652a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d652a-125">INPUTS</span></span>

### <span data-ttu-id="d652a-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d652a-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d652a-127">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d652a-127">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d652a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d652a-128">OUTPUTS</span></span>

### <span data-ttu-id="d652a-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d652a-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d652a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d652a-130">NOTES</span></span>

## <span data-ttu-id="d652a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d652a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d652a-132">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d652a-132">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d652a-133">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d652a-133">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="d652a-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d652a-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d652a-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d652a-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d652a-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d652a-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


