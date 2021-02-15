---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117471"
---
# <span data-ttu-id="12745-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12745-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="12745-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12745-102">SYNOPSIS</span></span>
<span data-ttu-id="12745-103">Adiciona uma configuração de pool de endereços back-end a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="12745-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="12745-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12745-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12745-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="12745-105">DESCRIPTION</span></span>
<span data-ttu-id="12745-106">O **cmdlet Add-AzLoadBalancerBackend** adiciona um pool de endereços back-end a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="12745-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="12745-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12745-107">EXAMPLES</span></span>

### <span data-ttu-id="12745-108">Exemplo 1: Adicionar uma configuração de pool de endereços back-end a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="12745-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="12745-109">Esse comando obtém o balanceador de carga chamado MyLoadBalancer, adiciona o pool de endereços back-end chamado BackendAddressPool02 ao MyLoadBalancer e usa o cmdlet **Set-AzLoadBalancer** para atualizar o MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="12745-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="12745-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12745-110">PARAMETERS</span></span>

### <span data-ttu-id="12745-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12745-111">-DefaultProfile</span></span>
<span data-ttu-id="12745-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="12745-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12745-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12745-113">-LoadBalancer</span></span>
<span data-ttu-id="12745-114">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="12745-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="12745-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="12745-115">-Name</span></span>
<span data-ttu-id="12745-116">Especifica o nome da configuração do pool de endereços de back-end a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="12745-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="12745-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="12745-117">-Confirm</span></span>
<span data-ttu-id="12745-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12745-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12745-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12745-119">-WhatIf</span></span>
<span data-ttu-id="12745-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="12745-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12745-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12745-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12745-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12745-122">CommonParameters</span></span>
<span data-ttu-id="12745-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12745-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12745-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12745-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12745-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="12745-125">INPUTS</span></span>

### <span data-ttu-id="12745-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12745-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12745-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="12745-127">OUTPUTS</span></span>

### <span data-ttu-id="12745-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12745-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12745-129">Notas</span><span class="sxs-lookup"><span data-stu-id="12745-129">NOTES</span></span>

## <span data-ttu-id="12745-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12745-130">RELATED LINKS</span></span>

[<span data-ttu-id="12745-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12745-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="12745-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="12745-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="12745-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12745-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="12745-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12745-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="12745-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="12745-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


