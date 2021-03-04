---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 30b66350cffeae7fa42da7c9230a9f3976ab6cc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890761"
---
# <span data-ttu-id="b7aee-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7aee-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b7aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7aee-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aee-103">Remove uma configuração de IP front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7aee-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="b7aee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7aee-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7aee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7aee-105">DESCRIPTION</span></span>
<span data-ttu-id="b7aee-106">O cmdlet **Remove-AzLoadBalancerFrontendIpConfig** remove uma configuração de IP front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7aee-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="b7aee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7aee-107">EXAMPLES</span></span>

### <span data-ttu-id="b7aee-108">Exemplo 1: Remover uma configuração de IP front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="b7aee-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b7aee-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP front-end que você deseja remover e o armazena na variável $loadbalancer front-end.</span><span class="sxs-lookup"><span data-stu-id="b7aee-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="b7aee-110">O segundo comando remove a configuração de IP frontend associada do balanceador de carga no $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="b7aee-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b7aee-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7aee-111">PARAMETERS</span></span>

### <span data-ttu-id="b7aee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aee-112">-DefaultProfile</span></span>
<span data-ttu-id="b7aee-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b7aee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7aee-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7aee-114">-LoadBalancer</span></span>
<span data-ttu-id="b7aee-115">Especifica o balanceador de carga que contém a configuração de IP front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b7aee-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="b7aee-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b7aee-116">-Name</span></span>
<span data-ttu-id="b7aee-117">Especifica o nome da configuração de endereço IP front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b7aee-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="b7aee-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7aee-118">-Confirm</span></span>
<span data-ttu-id="b7aee-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7aee-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7aee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7aee-120">-WhatIf</span></span>
<span data-ttu-id="b7aee-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7aee-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7aee-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7aee-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7aee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aee-123">CommonParameters</span></span>
<span data-ttu-id="b7aee-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7aee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aee-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7aee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aee-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7aee-126">INPUTS</span></span>

### <span data-ttu-id="b7aee-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7aee-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b7aee-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7aee-128">OUTPUTS</span></span>

### <span data-ttu-id="b7aee-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7aee-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b7aee-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7aee-130">NOTES</span></span>

## <span data-ttu-id="b7aee-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7aee-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7aee-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7aee-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7aee-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7aee-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b7aee-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7aee-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7aee-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7aee-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b7aee-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7aee-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


