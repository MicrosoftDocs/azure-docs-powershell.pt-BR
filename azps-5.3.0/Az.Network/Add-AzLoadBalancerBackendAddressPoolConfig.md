---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433495"
---
# <span data-ttu-id="31939-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31939-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="31939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31939-102">SYNOPSIS</span></span>
<span data-ttu-id="31939-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="31939-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="31939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31939-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31939-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31939-105">DESCRIPTION</span></span>
<span data-ttu-id="31939-106">O cmdlet **Add-AzLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="31939-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="31939-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31939-107">EXAMPLES</span></span>

### <span data-ttu-id="31939-108">Exemplo 1: adicionar uma configuração de pool de endereços de back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="31939-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="31939-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 a MyLoadBalancer e, em seguida, usa o cmdlet **set-AzLoadBalancer** para atualizar MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="31939-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="31939-110">OS</span><span class="sxs-lookup"><span data-stu-id="31939-110">PARAMETERS</span></span>

### <span data-ttu-id="31939-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31939-111">-DefaultProfile</span></span>
<span data-ttu-id="31939-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31939-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31939-113">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="31939-113">-LoadBalancer</span></span>
<span data-ttu-id="31939-114">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="31939-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="31939-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="31939-115">-Name</span></span>
<span data-ttu-id="31939-116">Especifica o nome da configuração do pool de endereços back-end a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="31939-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="31939-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31939-117">-Confirm</span></span>
<span data-ttu-id="31939-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31939-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31939-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31939-119">-WhatIf</span></span>
<span data-ttu-id="31939-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31939-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31939-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31939-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31939-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31939-122">CommonParameters</span></span>
<span data-ttu-id="31939-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31939-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31939-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31939-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31939-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31939-125">INPUTS</span></span>

### <span data-ttu-id="31939-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31939-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="31939-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31939-127">OUTPUTS</span></span>

### <span data-ttu-id="31939-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31939-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="31939-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31939-129">NOTES</span></span>

## <span data-ttu-id="31939-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31939-130">RELATED LINKS</span></span>

[<span data-ttu-id="31939-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31939-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="31939-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="31939-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="31939-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31939-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="31939-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31939-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="31939-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31939-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


