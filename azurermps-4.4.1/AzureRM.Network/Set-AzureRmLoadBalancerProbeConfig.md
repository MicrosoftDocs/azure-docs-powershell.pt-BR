---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9a6999dc379a5a39acea9b17107cabf2cae5ee25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429240"
---
# <span data-ttu-id="c50e0-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c50e0-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c50e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c50e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c50e0-103">Define o estado da meta para uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="c50e0-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c50e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c50e0-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c50e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c50e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c50e0-106">O cmdlet **set-AzureRmLoadBalancerProbeConfig** define o estado da meta para uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="c50e0-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="c50e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c50e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c50e0-108">Exemplo 1: modificar a configuração de teste em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="c50e0-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="c50e0-109">O primeiro comando obtém o loadbalancer chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="c50e0-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="c50e0-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzureRmLoadBalancerProbeConfig, o que adiciona uma nova configuração de sonda a ele.</span><span class="sxs-lookup"><span data-stu-id="c50e0-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="c50e0-111">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancerProbeConfig** , que define a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="c50e0-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="c50e0-112">Observe que é necessário especificar vários dos mesmos parâmetros que foram especificados no comando anterior porque são exigidos pelo cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="c50e0-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="c50e0-113">OS</span><span class="sxs-lookup"><span data-stu-id="c50e0-113">PARAMETERS</span></span>

### <span data-ttu-id="c50e0-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c50e0-114">-IntervalInSeconds</span></span>
<span data-ttu-id="c50e0-115">Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="c50e0-115">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e0-116">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="c50e0-116">-LoadBalancer</span></span>
<span data-ttu-id="c50e0-117">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c50e0-117">Specifies a load balancer.</span></span>
<span data-ttu-id="c50e0-118">Esse cmdlet define o estado da meta para uma configuração de teste para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c50e0-118">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c50e0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c50e0-119">-Name</span></span>
<span data-ttu-id="c50e0-120">Especifica o nome da configuração de sondagem que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="c50e0-120">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c50e0-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="c50e0-121">-Port</span></span>
<span data-ttu-id="c50e0-122">Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="c50e0-122">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e0-123">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="c50e0-123">-ProbeCount</span></span>
<span data-ttu-id="c50e0-124">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="c50e0-124">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e0-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="c50e0-125">-Protocol</span></span>
<span data-ttu-id="c50e0-126">Especifica o protocolo a ser usado para a sondagem.</span><span class="sxs-lookup"><span data-stu-id="c50e0-126">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="c50e0-127">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="c50e0-127">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e0-128">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="c50e0-128">-RequestPath</span></span>
<span data-ttu-id="c50e0-129">Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="c50e0-129">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="c50e0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50e0-130">-DefaultProfile</span></span>
<span data-ttu-id="c50e0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c50e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50e0-132">CommonParameters</span></span>
<span data-ttu-id="c50e0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c50e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50e0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c50e0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50e0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c50e0-135">INPUTS</span></span>

### <span data-ttu-id="c50e0-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50e0-136">PSLoadBalancer</span></span>
<span data-ttu-id="c50e0-137">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c50e0-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c50e0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c50e0-138">OUTPUTS</span></span>

### <span data-ttu-id="c50e0-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50e0-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c50e0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c50e0-140">NOTES</span></span>

## <span data-ttu-id="c50e0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c50e0-141">RELATED LINKS</span></span>

[<span data-ttu-id="c50e0-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c50e0-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c50e0-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50e0-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c50e0-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c50e0-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c50e0-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c50e0-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c50e0-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c50e0-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


