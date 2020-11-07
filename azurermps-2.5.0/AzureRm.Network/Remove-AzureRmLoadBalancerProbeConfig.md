---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: bed9eebb8812c0bd75eb19c3e8666d6a3b418a13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786418"
---
# <span data-ttu-id="514a1-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="514a1-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="514a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="514a1-102">SYNOPSIS</span></span>
<span data-ttu-id="514a1-103">Remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="514a1-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="514a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="514a1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="514a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="514a1-105">DESCRIPTION</span></span>
<span data-ttu-id="514a1-106">O cmdlet **Remove-AzureRmLoadBalancerProbeConfig** remove uma configuração de teste de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="514a1-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="514a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="514a1-107">EXAMPLES</span></span>

### <span data-ttu-id="514a1-108">Exemplo 1: remover uma configuração de teste de um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="514a1-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="514a1-109">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="514a1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="514a1-110">O segundo comando exclui a configuração nomeada myprobe do balanceador de carga em $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="514a1-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="514a1-111">OS</span><span class="sxs-lookup"><span data-stu-id="514a1-111">PARAMETERS</span></span>

### <span data-ttu-id="514a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514a1-112">-DefaultProfile</span></span>
<span data-ttu-id="514a1-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="514a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="514a1-114">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="514a1-114">-LoadBalancer</span></span>
<span data-ttu-id="514a1-115">Especifica o balanceador de carga que contém a configuração de sonda que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="514a1-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="514a1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="514a1-116">-Name</span></span>
<span data-ttu-id="514a1-117">Especifica o nome da configuração de sondagem que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="514a1-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="514a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514a1-118">CommonParameters</span></span>
<span data-ttu-id="514a1-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514a1-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514a1-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="514a1-121">INPUTS</span></span>

### <span data-ttu-id="514a1-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="514a1-122">PSLoadBalancer</span></span>
<span data-ttu-id="514a1-123">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="514a1-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="514a1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="514a1-124">OUTPUTS</span></span>

### <span data-ttu-id="514a1-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="514a1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="514a1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="514a1-126">NOTES</span></span>

## <span data-ttu-id="514a1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="514a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="514a1-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="514a1-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="514a1-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="514a1-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="514a1-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="514a1-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="514a1-131">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="514a1-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="514a1-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="514a1-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


