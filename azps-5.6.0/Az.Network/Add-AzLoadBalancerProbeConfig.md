---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 622501a69632be9c9c70cfccaf4e806df94e7276
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892462"
---
# <span data-ttu-id="2ed74-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ed74-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2ed74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed74-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed74-103">Adiciona uma configuração de sonda a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2ed74-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="2ed74-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ed74-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed74-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ed74-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed74-106">O cmdlet **Add-AzLoadBalancerProbeConfig** adiciona uma configuração de sonda a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed74-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="2ed74-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ed74-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed74-108">Exemplo 1: Adicionar uma configuração de sonda a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="2ed74-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="2ed74-109">Este comando obtém o balanceador de carga chamado myLb, adiciona a configuração da sonda especificada a ele e usa o cmdlet **Set-AzLoadBalancer** para atualizar o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2ed74-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="2ed74-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ed74-110">PARAMETERS</span></span>

### <span data-ttu-id="2ed74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed74-111">-DefaultProfile</span></span>
<span data-ttu-id="2ed74-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2ed74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed74-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2ed74-113">-IntervalInSeconds</span></span>
<span data-ttu-id="2ed74-114">Especifica o intervalo, em segundos, entre sondas para cada instância do serviço balanceado de carga.</span><span class="sxs-lookup"><span data-stu-id="2ed74-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="2ed74-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ed74-115">-LoadBalancer</span></span>
<span data-ttu-id="2ed74-116">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="2ed74-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="2ed74-117">Este cmdlet adiciona uma configuração de sonda ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2ed74-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ed74-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2ed74-118">-Name</span></span>
<span data-ttu-id="2ed74-119">Especifica o nome da configuração da sonda a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="2ed74-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="2ed74-120">-Port</span><span class="sxs-lookup"><span data-stu-id="2ed74-120">-Port</span></span>
<span data-ttu-id="2ed74-121">Especifica a porta na qual as sondas devem se conectar a um serviço com balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="2ed74-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="2ed74-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="2ed74-122">-ProbeCount</span></span>
<span data-ttu-id="2ed74-123">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada insalubre.</span><span class="sxs-lookup"><span data-stu-id="2ed74-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="2ed74-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2ed74-124">-Protocol</span></span>
<span data-ttu-id="2ed74-125">Especifica o protocolo a ser usado para a sonda.</span><span class="sxs-lookup"><span data-stu-id="2ed74-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="2ed74-126">Os valores aceitáveis para este parâmetro são: Tcp ou Http.</span><span class="sxs-lookup"><span data-stu-id="2ed74-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="2ed74-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="2ed74-127">-RequestPath</span></span>
<span data-ttu-id="2ed74-128">Especifica o caminho no serviço balanceado de carga para sondar para determinar a saúde.</span><span class="sxs-lookup"><span data-stu-id="2ed74-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="2ed74-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ed74-129">-Confirm</span></span>
<span data-ttu-id="2ed74-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed74-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed74-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed74-131">-WhatIf</span></span>
<span data-ttu-id="2ed74-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ed74-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ed74-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ed74-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed74-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed74-134">CommonParameters</span></span>
<span data-ttu-id="2ed74-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed74-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed74-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed74-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed74-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ed74-137">INPUTS</span></span>

### <span data-ttu-id="2ed74-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ed74-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2ed74-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2ed74-139">System.String</span></span>

### <span data-ttu-id="2ed74-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2ed74-140">System.Int32</span></span>

## <span data-ttu-id="2ed74-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ed74-141">OUTPUTS</span></span>

### <span data-ttu-id="2ed74-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ed74-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ed74-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ed74-143">NOTES</span></span>

## <span data-ttu-id="2ed74-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ed74-144">RELATED LINKS</span></span>

[<span data-ttu-id="2ed74-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ed74-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ed74-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ed74-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ed74-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ed74-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2ed74-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ed74-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="2ed74-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2ed74-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


