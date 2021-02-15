---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117470"
---
# <span data-ttu-id="f34aa-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f34aa-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f34aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f34aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f34aa-103">Adiciona uma configuração de configuração de configuração de configuração a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f34aa-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="f34aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f34aa-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f34aa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f34aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f34aa-106">O cmdlet **Add-AzLoadBalancerProbeConfig** adiciona uma configuração de configuração a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f34aa-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f34aa-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f34aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f34aa-108">Exemplo 1: Adicionar uma configuração de configuração de configuração de configuração a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f34aa-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="f34aa-109">Esse comando obtém o balanceador de carga chamado myLb, adiciona a configuração de configuração especificada a ele e usa o cmdlet **Set-AzLoadBalancer** para atualizar o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f34aa-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="f34aa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f34aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f34aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34aa-111">-DefaultProfile</span></span>
<span data-ttu-id="f34aa-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f34aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f34aa-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f34aa-113">-IntervalInSeconds</span></span>
<span data-ttu-id="f34aa-114">Especifica o intervalo, em segundos, entre intervalos para cada instância do serviço balanceado de carga.</span><span class="sxs-lookup"><span data-stu-id="f34aa-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="f34aa-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f34aa-115">-LoadBalancer</span></span>
<span data-ttu-id="f34aa-116">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="f34aa-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f34aa-117">Este cmdlet adiciona uma configuração de configuração ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f34aa-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f34aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f34aa-118">-Name</span></span>
<span data-ttu-id="f34aa-119">Especifica o nome da configuração de configuração de configuração para adicionar.</span><span class="sxs-lookup"><span data-stu-id="f34aa-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="f34aa-120">-Porta</span><span class="sxs-lookup"><span data-stu-id="f34aa-120">-Port</span></span>
<span data-ttu-id="f34aa-121">Especifica a porta na qual as cargas devem se conectar a um serviço balanceado de carga.</span><span class="sxs-lookup"><span data-stu-id="f34aa-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="f34aa-122">-Count</span><span class="sxs-lookup"><span data-stu-id="f34aa-122">-ProbeCount</span></span>
<span data-ttu-id="f34aa-123">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada insalubre.</span><span class="sxs-lookup"><span data-stu-id="f34aa-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="f34aa-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f34aa-124">-Protocol</span></span>
<span data-ttu-id="f34aa-125">Especifica o protocolo a ser usado para a busca.</span><span class="sxs-lookup"><span data-stu-id="f34aa-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="f34aa-126">Os valores aceitáveis para este parâmetro são: Tcp ou Http.</span><span class="sxs-lookup"><span data-stu-id="f34aa-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="f34aa-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="f34aa-127">-RequestPath</span></span>
<span data-ttu-id="f34aa-128">Especifica o caminho no serviço balanceado de carga para determinar a saúde.</span><span class="sxs-lookup"><span data-stu-id="f34aa-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="f34aa-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f34aa-129">-Confirm</span></span>
<span data-ttu-id="f34aa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f34aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f34aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f34aa-131">-WhatIf</span></span>
<span data-ttu-id="f34aa-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f34aa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f34aa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f34aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f34aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34aa-134">CommonParameters</span></span>
<span data-ttu-id="f34aa-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f34aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34aa-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34aa-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="f34aa-137">INPUTS</span></span>

### <span data-ttu-id="f34aa-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f34aa-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f34aa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f34aa-139">System.String</span></span>

### <span data-ttu-id="f34aa-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f34aa-140">System.Int32</span></span>

## <span data-ttu-id="f34aa-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="f34aa-141">OUTPUTS</span></span>

### <span data-ttu-id="f34aa-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f34aa-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f34aa-143">Notas</span><span class="sxs-lookup"><span data-stu-id="f34aa-143">NOTES</span></span>

## <span data-ttu-id="f34aa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f34aa-144">RELATED LINKS</span></span>

[<span data-ttu-id="f34aa-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f34aa-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f34aa-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f34aa-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f34aa-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f34aa-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f34aa-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f34aa-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="f34aa-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f34aa-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


