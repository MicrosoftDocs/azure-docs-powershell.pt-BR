---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602470"
---
# <span data-ttu-id="6eef2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6eef2-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="6eef2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eef2-102">SYNOPSIS</span></span>
<span data-ttu-id="6eef2-103">Remove uma configuração de pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6eef2-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eef2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eef2-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eef2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6eef2-105">DESCRIPTION</span></span>
<span data-ttu-id="6eef2-106">O cmdlet **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** remove um pool de endereços back-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6eef2-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="6eef2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6eef2-107">EXAMPLES</span></span>

### <span data-ttu-id="6eef2-108">Exemplo 1: remover uma configuração de pool de endereços de back-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="6eef2-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="6eef2-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer e o passa para **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , que remove a configuração BackendAddressPool02 do MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="6eef2-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="6eef2-110">Por fim, o cmdlet Set-AzureRmLoadBalancer atualiza MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="6eef2-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="6eef2-111">Observe que uma configuração de pool de endereços back-end deve existir antes que você possa excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="6eef2-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="6eef2-112">OS</span><span class="sxs-lookup"><span data-stu-id="6eef2-112">PARAMETERS</span></span>

### <span data-ttu-id="6eef2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eef2-113">-DefaultProfile</span></span>
<span data-ttu-id="6eef2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eef2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eef2-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="6eef2-115">-LoadBalancer</span></span>
<span data-ttu-id="6eef2-116">Especifica o balanceador de carga que contém o pool de endereços de back-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6eef2-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="6eef2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eef2-117">-Name</span></span>
<span data-ttu-id="6eef2-118">Especifica o nome do pool de endereços back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6eef2-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6eef2-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6eef2-119">-Confirm</span></span>
<span data-ttu-id="6eef2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eef2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eef2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eef2-121">-WhatIf</span></span>
<span data-ttu-id="6eef2-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6eef2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eef2-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6eef2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eef2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eef2-124">CommonParameters</span></span>
<span data-ttu-id="6eef2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eef2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eef2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eef2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eef2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6eef2-127">INPUTS</span></span>

### <span data-ttu-id="6eef2-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6eef2-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="6eef2-129">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6eef2-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="6eef2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6eef2-130">OUTPUTS</span></span>

### <span data-ttu-id="6eef2-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6eef2-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6eef2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6eef2-132">NOTES</span></span>

## <span data-ttu-id="6eef2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eef2-133">RELATED LINKS</span></span>

[<span data-ttu-id="6eef2-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6eef2-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6eef2-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6eef2-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="6eef2-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6eef2-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6eef2-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6eef2-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


