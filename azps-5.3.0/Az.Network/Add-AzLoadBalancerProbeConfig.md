---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428201"
---
# <span data-ttu-id="cefb5-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefb5-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="cefb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cefb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cefb5-103">Adiciona uma configuração de teste a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="cefb5-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="cefb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cefb5-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cefb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cefb5-105">DESCRIPTION</span></span>
<span data-ttu-id="cefb5-106">O cmdlet **Add-AzLoadBalancerProbeConfig** adiciona uma configuração de teste a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="cefb5-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="cefb5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cefb5-107">EXAMPLES</span></span>

### <span data-ttu-id="cefb5-108">Exemplo 1: adicionar uma configuração de teste a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="cefb5-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="cefb5-109">Esse comando obtém o balanceador de carga chamado myLb, adiciona a configuração de teste especificada a ele e, em seguida, usa o cmdlet **set-AzLoadBalancer** para atualizar o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="cefb5-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="cefb5-110">OS</span><span class="sxs-lookup"><span data-stu-id="cefb5-110">PARAMETERS</span></span>

### <span data-ttu-id="cefb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefb5-111">-DefaultProfile</span></span>
<span data-ttu-id="cefb5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cefb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cefb5-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cefb5-113">-IntervalInSeconds</span></span>
<span data-ttu-id="cefb5-114">Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="cefb5-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="cefb5-115">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="cefb5-115">-LoadBalancer</span></span>
<span data-ttu-id="cefb5-116">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="cefb5-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="cefb5-117">Esse cmdlet adiciona uma configuração de teste ao balanceador de carga que o parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cefb5-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="cefb5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cefb5-118">-Name</span></span>
<span data-ttu-id="cefb5-119">Especifica o nome da configuração de sonda a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="cefb5-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="cefb5-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="cefb5-120">-Port</span></span>
<span data-ttu-id="cefb5-121">Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="cefb5-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="cefb5-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="cefb5-122">-ProbeCount</span></span>
<span data-ttu-id="cefb5-123">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="cefb5-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="cefb5-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="cefb5-124">-Protocol</span></span>
<span data-ttu-id="cefb5-125">Especifica o protocolo a ser usado para o teste.</span><span class="sxs-lookup"><span data-stu-id="cefb5-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="cefb5-126">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="cefb5-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="cefb5-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="cefb5-127">-RequestPath</span></span>
<span data-ttu-id="cefb5-128">Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="cefb5-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="cefb5-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cefb5-129">-Confirm</span></span>
<span data-ttu-id="cefb5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cefb5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefb5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefb5-131">-WhatIf</span></span>
<span data-ttu-id="cefb5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cefb5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cefb5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cefb5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefb5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefb5-134">CommonParameters</span></span>
<span data-ttu-id="cefb5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefb5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefb5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefb5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefb5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cefb5-137">INPUTS</span></span>

### <span data-ttu-id="cefb5-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cefb5-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="cefb5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cefb5-139">System.String</span></span>

### <span data-ttu-id="cefb5-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cefb5-140">System.Int32</span></span>

## <span data-ttu-id="cefb5-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cefb5-141">OUTPUTS</span></span>

### <span data-ttu-id="cefb5-142">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cefb5-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cefb5-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cefb5-143">NOTES</span></span>

## <span data-ttu-id="cefb5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cefb5-144">RELATED LINKS</span></span>

[<span data-ttu-id="cefb5-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefb5-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefb5-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefb5-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefb5-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefb5-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefb5-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cefb5-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="cefb5-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefb5-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


