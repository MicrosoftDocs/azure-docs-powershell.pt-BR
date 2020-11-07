---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772366"
---
# <span data-ttu-id="2a80b-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2a80b-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2a80b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a80b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a80b-103">Cria uma configuração de sondagem para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a80b-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="2a80b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a80b-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a80b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a80b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a80b-106">O cmdlet **New-AzLoadBalancerProbeConfig** cria uma configuração de teste para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a80b-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2a80b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a80b-107">EXAMPLES</span></span>

### <span data-ttu-id="2a80b-108">Exemplo 1: criar uma configuração de sondagem</span><span class="sxs-lookup"><span data-stu-id="2a80b-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="2a80b-109">Esse comando cria uma configuração de sondagem chamada myprobe usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a80b-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="2a80b-110">O novo teste será conectado a um serviço de balanceamento de carga na porta 80.</span><span class="sxs-lookup"><span data-stu-id="2a80b-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="2a80b-111">OS</span><span class="sxs-lookup"><span data-stu-id="2a80b-111">PARAMETERS</span></span>

### <span data-ttu-id="2a80b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a80b-112">-DefaultProfile</span></span>
<span data-ttu-id="2a80b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a80b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a80b-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2a80b-114">-IntervalInSeconds</span></span>
<span data-ttu-id="2a80b-115">Especifica o intervalo, em segundos, entre testes para cada instância de um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="2a80b-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="2a80b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a80b-116">-Name</span></span>
<span data-ttu-id="2a80b-117">Especifica o nome da configuração de sonda a ser criada.</span><span class="sxs-lookup"><span data-stu-id="2a80b-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="2a80b-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="2a80b-118">-Port</span></span>
<span data-ttu-id="2a80b-119">Especifica a porta na qual o novo teste deve se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="2a80b-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="2a80b-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="2a80b-120">-ProbeCount</span></span>
<span data-ttu-id="2a80b-121">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="2a80b-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="2a80b-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2a80b-122">-Protocol</span></span>
<span data-ttu-id="2a80b-123">Especifica o protocolo a ser usado para a configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="2a80b-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="2a80b-124">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="2a80b-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="2a80b-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="2a80b-125">-RequestPath</span></span>
<span data-ttu-id="2a80b-126">Especifica o caminho em um serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="2a80b-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="2a80b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a80b-127">-Confirm</span></span>
<span data-ttu-id="2a80b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a80b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a80b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a80b-129">-WhatIf</span></span>
<span data-ttu-id="2a80b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a80b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a80b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a80b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a80b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a80b-132">CommonParameters</span></span>
<span data-ttu-id="2a80b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a80b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a80b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a80b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a80b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a80b-135">INPUTS</span></span>

### <span data-ttu-id="2a80b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2a80b-136">System.String</span></span>

### <span data-ttu-id="2a80b-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2a80b-137">System.Int32</span></span>

## <span data-ttu-id="2a80b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a80b-138">OUTPUTS</span></span>

### <span data-ttu-id="2a80b-139">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="2a80b-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="2a80b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a80b-140">NOTES</span></span>

## <span data-ttu-id="2a80b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a80b-141">RELATED LINKS</span></span>

[<span data-ttu-id="2a80b-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2a80b-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2a80b-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2a80b-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2a80b-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2a80b-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2a80b-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2a80b-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


