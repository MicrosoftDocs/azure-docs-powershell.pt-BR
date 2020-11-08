---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116079"
---
# <span data-ttu-id="690f9-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="690f9-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="690f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="690f9-102">SYNOPSIS</span></span>
<span data-ttu-id="690f9-103">Remove uma configuração de pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="690f9-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="690f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="690f9-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="690f9-105">DESCRIPTION</span></span>
<span data-ttu-id="690f9-106">O cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="690f9-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="690f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="690f9-107">EXAMPLES</span></span>

### <span data-ttu-id="690f9-108">Exemplo 1: remover uma configuração de pool de endereços de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="690f9-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="690f9-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer e o passa para **Remove-AzLoadBalancerBackendAddressPoolConfig** , que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="690f9-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="690f9-110">Por fim, o cmdlet Set-AzLoadBalancer atualiza MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="690f9-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="690f9-111">Observe que uma configuração de pool de endereços back-end deve existir antes que você possa excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="690f9-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="690f9-112">OS</span><span class="sxs-lookup"><span data-stu-id="690f9-112">PARAMETERS</span></span>

### <span data-ttu-id="690f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690f9-113">-DefaultProfile</span></span>
<span data-ttu-id="690f9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="690f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690f9-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="690f9-115">-LoadBalancer</span></span>
<span data-ttu-id="690f9-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="690f9-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="690f9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="690f9-117">-Name</span></span>
<span data-ttu-id="690f9-118">Especifica o nome do pool de endereços back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="690f9-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="690f9-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="690f9-119">-Confirm</span></span>
<span data-ttu-id="690f9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690f9-121">-WhatIf</span></span>
<span data-ttu-id="690f9-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="690f9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="690f9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="690f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="690f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690f9-124">CommonParameters</span></span>
<span data-ttu-id="690f9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690f9-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690f9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="690f9-127">INPUTS</span></span>

### <span data-ttu-id="690f9-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="690f9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="690f9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="690f9-129">OUTPUTS</span></span>

### <span data-ttu-id="690f9-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="690f9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="690f9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="690f9-131">NOTES</span></span>

## <span data-ttu-id="690f9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="690f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="690f9-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="690f9-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="690f9-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="690f9-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="690f9-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="690f9-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="690f9-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="690f9-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


