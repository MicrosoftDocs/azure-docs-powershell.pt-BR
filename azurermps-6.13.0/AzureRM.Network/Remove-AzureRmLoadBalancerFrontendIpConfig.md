---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 1a71b48387948d65ba0db24fdb2c236a11a9a44d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441232"
---
# <span data-ttu-id="eeec1-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeec1-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="eeec1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eeec1-102">SYNOPSIS</span></span>
<span data-ttu-id="eeec1-103">Remove uma configuração de IP de front-end de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="eeec1-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eeec1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeec1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eeec1-105">DESCRIPTION</span></span>
<span data-ttu-id="eeec1-106">O cmdlet **Remove-AzureRmLoadBalancerFrontendIpConfig** remove uma configuração de IP de front-end de um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="eeec1-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="eeec1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eeec1-107">EXAMPLES</span></span>

### <span data-ttu-id="eeec1-108">Exemplo 1: remover uma configuração de IP de front-end de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="eeec1-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="eeec1-109">O primeiro comando obtém o balanceador de carga associado à configuração de IP de front-end que você deseja remover e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="eeec1-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="eeec1-110">O segundo comando Remove a configuração de IP de front-end associada do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="eeec1-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="eeec1-111">OS</span><span class="sxs-lookup"><span data-stu-id="eeec1-111">PARAMETERS</span></span>

### <span data-ttu-id="eeec1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeec1-112">-DefaultProfile</span></span>
<span data-ttu-id="eeec1-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eeec1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeec1-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="eeec1-114">-LoadBalancer</span></span>
<span data-ttu-id="eeec1-115">Especifica o balanceador de carga que contém a configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="eeec1-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="eeec1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeec1-116">-Name</span></span>
<span data-ttu-id="eeec1-117">Especifica o nome da configuração de endereço IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="eeec1-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="eeec1-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eeec1-118">-Confirm</span></span>
<span data-ttu-id="eeec1-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeec1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeec1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeec1-120">-WhatIf</span></span>
<span data-ttu-id="eeec1-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eeec1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeec1-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eeec1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeec1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeec1-123">CommonParameters</span></span>
<span data-ttu-id="eeec1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeec1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeec1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeec1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeec1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eeec1-126">INPUTS</span></span>

### <span data-ttu-id="eeec1-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeec1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="eeec1-128">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eeec1-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="eeec1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eeec1-129">OUTPUTS</span></span>

### <span data-ttu-id="eeec1-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeec1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eeec1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eeec1-131">NOTES</span></span>

## <span data-ttu-id="eeec1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eeec1-132">RELATED LINKS</span></span>

[<span data-ttu-id="eeec1-133">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeec1-133">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eeec1-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eeec1-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="eeec1-135">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeec1-135">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eeec1-136">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeec1-136">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eeec1-137">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeec1-137">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


