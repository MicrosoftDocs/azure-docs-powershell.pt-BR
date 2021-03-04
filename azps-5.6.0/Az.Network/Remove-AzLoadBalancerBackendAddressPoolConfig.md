---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 08644bd8b9846b0eb7d647b3df9c12008070c059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890763"
---
# <span data-ttu-id="97cee-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="97cee-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="97cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97cee-102">SYNOPSIS</span></span>
<span data-ttu-id="97cee-103">Remove uma configuração de pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="97cee-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="97cee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="97cee-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97cee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97cee-105">DESCRIPTION</span></span>
<span data-ttu-id="97cee-106">O cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="97cee-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="97cee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97cee-107">EXAMPLES</span></span>

### <span data-ttu-id="97cee-108">Exemplo 1: Remover uma configuração de pool de endereços back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="97cee-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="97cee-109">Este comando obtém o balanceador de carga chamado MyLoadBalancer e o passa para **Remove-AzLoadBalancerBackendAddressPoolConfig**, que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="97cee-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="97cee-110">Finalmente, o cmdlet Set-AzLoadBalancer atualiza MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="97cee-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="97cee-111">Observe que uma configuração de pool de endereços back-end deve existir antes de poder excluí-la.</span><span class="sxs-lookup"><span data-stu-id="97cee-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="97cee-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="97cee-112">PARAMETERS</span></span>

### <span data-ttu-id="97cee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cee-113">-DefaultProfile</span></span>
<span data-ttu-id="97cee-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="97cee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97cee-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97cee-115">-LoadBalancer</span></span>
<span data-ttu-id="97cee-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="97cee-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="97cee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="97cee-117">-Name</span></span>
<span data-ttu-id="97cee-118">Especifica o nome do pool de endereços back-end que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="97cee-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="97cee-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97cee-119">-Confirm</span></span>
<span data-ttu-id="97cee-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97cee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97cee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97cee-121">-WhatIf</span></span>
<span data-ttu-id="97cee-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97cee-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97cee-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97cee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97cee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cee-124">CommonParameters</span></span>
<span data-ttu-id="97cee-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cee-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97cee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cee-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97cee-127">INPUTS</span></span>

### <span data-ttu-id="97cee-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97cee-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="97cee-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="97cee-129">OUTPUTS</span></span>

### <span data-ttu-id="97cee-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97cee-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="97cee-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="97cee-131">NOTES</span></span>

## <span data-ttu-id="97cee-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97cee-132">RELATED LINKS</span></span>

[<span data-ttu-id="97cee-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="97cee-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="97cee-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97cee-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="97cee-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="97cee-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="97cee-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="97cee-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


