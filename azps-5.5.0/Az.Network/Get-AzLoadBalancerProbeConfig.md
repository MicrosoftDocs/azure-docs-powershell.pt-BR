---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115176"
---
# <span data-ttu-id="aa7c5-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="aa7c5-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="aa7c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7c5-103">Obtém uma configuração de configuração de configuração para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="aa7c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa7c5-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa7c5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="aa7c5-106">O cmdlet **Get-AzLoadBalancerProbeConfig obtém** uma ou mais configurações de configuração de configuração para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="aa7c5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="aa7c5-108">Exemplo 1: Obter a configuração de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="aa7c5-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="aa7c5-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="aa7c5-110">O segundo comando obtém a configuração de configuração associada chamada MyProbe do balanceador de carga no $slb.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="aa7c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa7c5-111">PARAMETERS</span></span>

### <span data-ttu-id="aa7c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7c5-112">-DefaultProfile</span></span>
<span data-ttu-id="aa7c5-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa7c5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aa7c5-114">-LoadBalancer</span></span>
<span data-ttu-id="aa7c5-115">Especifica o balanceador de carga associado à configuração de configuração para obter.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="aa7c5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa7c5-116">-Name</span></span>
<span data-ttu-id="aa7c5-117">Especifica o nome da configuração de configuração de configuração para obter.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="aa7c5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7c5-118">CommonParameters</span></span>
<span data-ttu-id="aa7c5-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7c5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7c5-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa7c5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7c5-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="aa7c5-121">INPUTS</span></span>

### <span data-ttu-id="aa7c5-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aa7c5-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aa7c5-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="aa7c5-123">OUTPUTS</span></span>

### <span data-ttu-id="aa7c5-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="aa7c5-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="aa7c5-125">Notas</span><span class="sxs-lookup"><span data-stu-id="aa7c5-125">NOTES</span></span>

## <span data-ttu-id="aa7c5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa7c5-126">RELATED LINKS</span></span>

[<span data-ttu-id="aa7c5-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="aa7c5-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="aa7c5-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aa7c5-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="aa7c5-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="aa7c5-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="aa7c5-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="aa7c5-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="aa7c5-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="aa7c5-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


