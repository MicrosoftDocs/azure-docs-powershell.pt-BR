---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954777"
---
# <span data-ttu-id="71c38-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c38-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="71c38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71c38-102">SYNOPSIS</span></span>
<span data-ttu-id="71c38-103">Atualiza uma configuração de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="71c38-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="71c38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71c38-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71c38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71c38-105">DESCRIPTION</span></span>
<span data-ttu-id="71c38-106">O cmdlet **set-AzLoadBalancerProbeConfig** atualiza uma configuração de teste para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="71c38-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="71c38-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71c38-107">EXAMPLES</span></span>

### <span data-ttu-id="71c38-108">Exemplo 1: modificar a configuração de teste em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="71c38-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="71c38-109">O primeiro comando obtém o loadbalancer chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="71c38-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="71c38-110">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerProbeConfig, o que adiciona uma nova configuração de sonda a ele.</span><span class="sxs-lookup"><span data-stu-id="71c38-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="71c38-111">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerProbeConfig** , que define a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="71c38-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="71c38-112">Observe que é necessário especificar vários dos mesmos parâmetros que foram especificados no comando anterior porque são exigidos pelo cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="71c38-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="71c38-113">OS</span><span class="sxs-lookup"><span data-stu-id="71c38-113">PARAMETERS</span></span>

### <span data-ttu-id="71c38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c38-114">-DefaultProfile</span></span>
<span data-ttu-id="71c38-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71c38-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c38-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="71c38-116">-IntervalInSeconds</span></span>
<span data-ttu-id="71c38-117">Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="71c38-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="71c38-118">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="71c38-118">-LoadBalancer</span></span>
<span data-ttu-id="71c38-119">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="71c38-119">Specifies a load balancer.</span></span>
<span data-ttu-id="71c38-120">Esse cmdlet atualiza uma configuração de teste para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="71c38-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="71c38-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="71c38-121">-Name</span></span>
<span data-ttu-id="71c38-122">Especifica o nome da configuração de sondagem que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="71c38-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="71c38-123">-Porta</span><span class="sxs-lookup"><span data-stu-id="71c38-123">-Port</span></span>
<span data-ttu-id="71c38-124">Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="71c38-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="71c38-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="71c38-125">-ProbeCount</span></span>
<span data-ttu-id="71c38-126">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="71c38-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="71c38-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="71c38-127">-Protocol</span></span>
<span data-ttu-id="71c38-128">Especifica o protocolo a ser usado para a sondagem.</span><span class="sxs-lookup"><span data-stu-id="71c38-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="71c38-129">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="71c38-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="71c38-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="71c38-130">-RequestPath</span></span>
<span data-ttu-id="71c38-131">Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="71c38-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="71c38-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71c38-132">-Confirm</span></span>
<span data-ttu-id="71c38-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c38-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c38-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c38-134">-WhatIf</span></span>
<span data-ttu-id="71c38-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71c38-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71c38-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71c38-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c38-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c38-137">CommonParameters</span></span>
<span data-ttu-id="71c38-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c38-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c38-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c38-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c38-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71c38-140">INPUTS</span></span>

### <span data-ttu-id="71c38-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71c38-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="71c38-142">System. String</span><span class="sxs-lookup"><span data-stu-id="71c38-142">System.String</span></span>

### <span data-ttu-id="71c38-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71c38-143">System.Int32</span></span>

## <span data-ttu-id="71c38-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71c38-144">OUTPUTS</span></span>

### <span data-ttu-id="71c38-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71c38-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="71c38-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71c38-146">NOTES</span></span>

## <span data-ttu-id="71c38-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71c38-147">RELATED LINKS</span></span>

[<span data-ttu-id="71c38-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c38-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71c38-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71c38-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="71c38-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c38-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71c38-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c38-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71c38-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71c38-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


