---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114117"
---
# <span data-ttu-id="e4a8d-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e4a8d-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e4a8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a8d-103">Remove uma configuração de pool de endereços de back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="e4a8d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4a8d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a8d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a8d-106">O cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="e4a8d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a8d-108">Exemplo 1: Remover uma configuração de pool de endereços back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="e4a8d-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="e4a8d-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer e **passa-o para Remove-AzLoadBalancerBackendAddressPoolConfig,** que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="e4a8d-110">Por fim, o Set-AzLoadBalancer cmdlet atualiza o MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="e4a8d-111">Observe que uma configuração de pool de endereços back-end deve existir antes que você possa excluí-la.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="e4a8d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4a8d-112">PARAMETERS</span></span>

### <span data-ttu-id="e4a8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a8d-113">-DefaultProfile</span></span>
<span data-ttu-id="e4a8d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4a8d-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e4a8d-115">-LoadBalancer</span></span>
<span data-ttu-id="e4a8d-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="e4a8d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4a8d-117">-Name</span></span>
<span data-ttu-id="e4a8d-118">Especifica o nome do pool de endereços de back-end que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4a8d-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4a8d-119">-Confirm</span></span>
<span data-ttu-id="e4a8d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a8d-121">-WhatIf</span></span>
<span data-ttu-id="e4a8d-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4a8d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a8d-124">CommonParameters</span></span>
<span data-ttu-id="e4a8d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a8d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a8d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a8d-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4a8d-127">INPUTS</span></span>

### <span data-ttu-id="e4a8d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e4a8d-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e4a8d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4a8d-129">OUTPUTS</span></span>

### <span data-ttu-id="e4a8d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e4a8d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e4a8d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e4a8d-131">NOTES</span></span>

## <span data-ttu-id="e4a8d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4a8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4a8d-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e4a8d-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e4a8d-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e4a8d-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e4a8d-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e4a8d-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e4a8d-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e4a8d-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


