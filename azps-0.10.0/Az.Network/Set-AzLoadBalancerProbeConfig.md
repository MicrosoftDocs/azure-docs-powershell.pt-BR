---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776534"
---
# <span data-ttu-id="12b9d-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="12b9d-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="12b9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="12b9d-103">Define o estado da meta para uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="12b9d-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="12b9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12b9d-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12b9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="12b9d-106">O cmdlet **set-AzLoadBalancerProbeConfig** define o estado da meta para uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="12b9d-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="12b9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="12b9d-108">Exemplo 1: modificar a configuração de teste em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="12b9d-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="12b9d-109">O primeiro comando obtém o loadbalancer chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="12b9d-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="12b9d-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerProbeConfig, o que adiciona uma nova configuração de sonda a ele.</span><span class="sxs-lookup"><span data-stu-id="12b9d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="12b9d-111">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerProbeConfig** , que define a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="12b9d-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="12b9d-112">Observe que é necessário especificar vários dos mesmos parâmetros que foram especificados no comando anterior porque são exigidos pelo cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="12b9d-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="12b9d-113">OS</span><span class="sxs-lookup"><span data-stu-id="12b9d-113">PARAMETERS</span></span>

### <span data-ttu-id="12b9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b9d-114">-DefaultProfile</span></span>
<span data-ttu-id="12b9d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12b9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b9d-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="12b9d-116">-IntervalInSeconds</span></span>
<span data-ttu-id="12b9d-117">Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="12b9d-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b9d-118">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="12b9d-118">-LoadBalancer</span></span>
<span data-ttu-id="12b9d-119">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="12b9d-119">Specifies a load balancer.</span></span>
<span data-ttu-id="12b9d-120">Esse cmdlet define o estado da meta para uma configuração de teste para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="12b9d-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="12b9d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="12b9d-121">-Name</span></span>
<span data-ttu-id="12b9d-122">Especifica o nome da configuração de sondagem que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="12b9d-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b9d-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="12b9d-123">-Port</span></span>
<span data-ttu-id="12b9d-124">Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="12b9d-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b9d-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="12b9d-125">-ProbeCount</span></span>
<span data-ttu-id="12b9d-126">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="12b9d-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b9d-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="12b9d-127">-Protocol</span></span>
<span data-ttu-id="12b9d-128">Especifica o protocolo a ser usado para a sondagem.</span><span class="sxs-lookup"><span data-stu-id="12b9d-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="12b9d-129">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="12b9d-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b9d-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="12b9d-130">-RequestPath</span></span>
<span data-ttu-id="12b9d-131">Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="12b9d-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="12b9d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b9d-132">CommonParameters</span></span>
<span data-ttu-id="12b9d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b9d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b9d-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b9d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b9d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12b9d-135">INPUTS</span></span>

### <span data-ttu-id="12b9d-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12b9d-136">PSLoadBalancer</span></span>
<span data-ttu-id="12b9d-137">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="12b9d-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="12b9d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12b9d-138">OUTPUTS</span></span>

### <span data-ttu-id="12b9d-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12b9d-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12b9d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12b9d-140">NOTES</span></span>

## <span data-ttu-id="12b9d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12b9d-141">RELATED LINKS</span></span>

[<span data-ttu-id="12b9d-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="12b9d-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="12b9d-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12b9d-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="12b9d-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="12b9d-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="12b9d-145">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="12b9d-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="12b9d-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="12b9d-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


