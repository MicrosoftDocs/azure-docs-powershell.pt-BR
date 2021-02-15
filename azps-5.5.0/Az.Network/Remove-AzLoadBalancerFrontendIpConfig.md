---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115089"
---
# <span data-ttu-id="0ce7d-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0ce7d-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0ce7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ce7d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce7d-103">Remove uma configuração IP front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="0ce7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ce7d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce7d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ce7d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce7d-106">O cmdlet **Remove-AzLoadBalancerFrontendIpConfig** remove uma configuração IP front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="0ce7d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ce7d-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce7d-108">Exemplo 1: Remover uma configuração IP front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0ce7d-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0ce7d-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP front-end que você deseja remover e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="0ce7d-110">O segundo comando remove a configuração IP frontend associada do balanceador de carga no $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0ce7d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ce7d-111">PARAMETERS</span></span>

### <span data-ttu-id="0ce7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce7d-112">-DefaultProfile</span></span>
<span data-ttu-id="0ce7d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce7d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ce7d-114">-LoadBalancer</span></span>
<span data-ttu-id="0ce7d-115">Especifica o balanceador de carga que contém a configuração IP front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="0ce7d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ce7d-116">-Name</span></span>
<span data-ttu-id="0ce7d-117">Especifica o nome da configuração de endereço IP front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="0ce7d-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0ce7d-118">-Confirm</span></span>
<span data-ttu-id="0ce7d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce7d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce7d-120">-WhatIf</span></span>
<span data-ttu-id="0ce7d-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ce7d-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce7d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce7d-123">CommonParameters</span></span>
<span data-ttu-id="0ce7d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce7d-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce7d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce7d-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ce7d-126">INPUTS</span></span>

### <span data-ttu-id="0ce7d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ce7d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0ce7d-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ce7d-128">OUTPUTS</span></span>

### <span data-ttu-id="0ce7d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ce7d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0ce7d-130">Notas</span><span class="sxs-lookup"><span data-stu-id="0ce7d-130">NOTES</span></span>

## <span data-ttu-id="0ce7d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ce7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ce7d-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0ce7d-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0ce7d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ce7d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0ce7d-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0ce7d-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0ce7d-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0ce7d-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0ce7d-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0ce7d-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


