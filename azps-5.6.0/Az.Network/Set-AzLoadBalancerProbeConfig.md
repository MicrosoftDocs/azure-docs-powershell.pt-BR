---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892080"
---
# <span data-ttu-id="10bdd-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="10bdd-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="10bdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="10bdd-103">Atualiza uma configuração de sonda para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10bdd-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="10bdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10bdd-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10bdd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="10bdd-106">O cmdlet **Set-AzLoadBalancerProbeConfig** atualiza uma configuração de sonda para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10bdd-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="10bdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="10bdd-108">Exemplo 1: Modificar a configuração da sonda em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="10bdd-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="10bdd-109">O primeiro comando obtém o loadbalancer chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="10bdd-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="10bdd-110">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerProbeConfig, que adiciona uma nova configuração de sonda a ele.</span><span class="sxs-lookup"><span data-stu-id="10bdd-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="10bdd-111">O terceiro comando passa o balanceador de carga para **Set-AzLoadBalancerProbeConfig**, que define a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="10bdd-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="10bdd-112">Observe que é necessário especificar vários dos mesmos parâmetros que foram especificados no comando anterior porque eles são exigidos pelo cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="10bdd-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="10bdd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10bdd-113">PARAMETERS</span></span>

### <span data-ttu-id="10bdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bdd-114">-DefaultProfile</span></span>
<span data-ttu-id="10bdd-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="10bdd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10bdd-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="10bdd-116">-IntervalInSeconds</span></span>
<span data-ttu-id="10bdd-117">Especifica o intervalo, em segundos, entre sondas para cada instância do serviço balanceado de carga.</span><span class="sxs-lookup"><span data-stu-id="10bdd-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bdd-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10bdd-118">-LoadBalancer</span></span>
<span data-ttu-id="10bdd-119">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10bdd-119">Specifies a load balancer.</span></span>
<span data-ttu-id="10bdd-120">Este cmdlet atualiza uma configuração de sonda para o balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10bdd-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="10bdd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="10bdd-121">-Name</span></span>
<span data-ttu-id="10bdd-122">Especifica o nome da configuração da sonda que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="10bdd-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="10bdd-123">-Port</span><span class="sxs-lookup"><span data-stu-id="10bdd-123">-Port</span></span>
<span data-ttu-id="10bdd-124">Especifica a porta na qual as sondas devem se conectar a um serviço com balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="10bdd-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bdd-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="10bdd-125">-ProbeCount</span></span>
<span data-ttu-id="10bdd-126">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada insalubre.</span><span class="sxs-lookup"><span data-stu-id="10bdd-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bdd-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="10bdd-127">-Protocol</span></span>
<span data-ttu-id="10bdd-128">Especifica o protocolo a ser usado para a sondagem.</span><span class="sxs-lookup"><span data-stu-id="10bdd-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="10bdd-129">Os valores aceitáveis para este parâmetro são: Tcp ou Http.</span><span class="sxs-lookup"><span data-stu-id="10bdd-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bdd-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="10bdd-130">-RequestPath</span></span>
<span data-ttu-id="10bdd-131">Especifica o caminho no serviço balanceado de carga para sondar para determinar a saúde.</span><span class="sxs-lookup"><span data-stu-id="10bdd-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bdd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10bdd-132">-Confirm</span></span>
<span data-ttu-id="10bdd-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10bdd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bdd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bdd-134">-WhatIf</span></span>
<span data-ttu-id="10bdd-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10bdd-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10bdd-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10bdd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bdd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bdd-137">CommonParameters</span></span>
<span data-ttu-id="10bdd-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10bdd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bdd-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10bdd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bdd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10bdd-140">INPUTS</span></span>

### <span data-ttu-id="10bdd-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10bdd-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="10bdd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="10bdd-142">System.String</span></span>

### <span data-ttu-id="10bdd-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="10bdd-143">System.Int32</span></span>

## <span data-ttu-id="10bdd-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10bdd-144">OUTPUTS</span></span>

### <span data-ttu-id="10bdd-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10bdd-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="10bdd-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="10bdd-146">NOTES</span></span>

## <span data-ttu-id="10bdd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10bdd-147">RELATED LINKS</span></span>

[<span data-ttu-id="10bdd-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="10bdd-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="10bdd-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="10bdd-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="10bdd-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="10bdd-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="10bdd-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="10bdd-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="10bdd-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="10bdd-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


