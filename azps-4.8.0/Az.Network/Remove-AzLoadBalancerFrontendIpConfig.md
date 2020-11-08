---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110483"
---
# <span data-ttu-id="3d9f2-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9f2-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="3d9f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9f2-103">Remove uma configuração de IP de front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="3d9f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d9f2-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d9f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9f2-106">O cmdlet **Remove-AzLoadBalancerFrontendIpConfig** remove uma configuração de IP de front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="3d9f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="3d9f2-108">Exemplo 1: remover uma configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="3d9f2-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="3d9f2-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP de front-end que você deseja remover e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="3d9f2-110">O segundo comando Remove a configuração de IP de front-end associada do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="3d9f2-111">OS</span><span class="sxs-lookup"><span data-stu-id="3d9f2-111">PARAMETERS</span></span>

### <span data-ttu-id="3d9f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9f2-112">-DefaultProfile</span></span>
<span data-ttu-id="3d9f2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d9f2-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="3d9f2-114">-LoadBalancer</span></span>
<span data-ttu-id="3d9f2-115">Especifica o balanceador de carga que contém a configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="3d9f2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d9f2-116">-Name</span></span>
<span data-ttu-id="3d9f2-117">Especifica o nome da configuração de endereço IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="3d9f2-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d9f2-118">-Confirm</span></span>
<span data-ttu-id="3d9f2-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d9f2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d9f2-120">-WhatIf</span></span>
<span data-ttu-id="3d9f2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d9f2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d9f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9f2-123">CommonParameters</span></span>
<span data-ttu-id="3d9f2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9f2-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9f2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9f2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d9f2-126">INPUTS</span></span>

### <span data-ttu-id="3d9f2-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d9f2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3d9f2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d9f2-128">OUTPUTS</span></span>

### <span data-ttu-id="3d9f2-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d9f2-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3d9f2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d9f2-130">NOTES</span></span>

## <span data-ttu-id="3d9f2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d9f2-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d9f2-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9f2-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3d9f2-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d9f2-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3d9f2-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9f2-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3d9f2-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9f2-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3d9f2-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d9f2-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


