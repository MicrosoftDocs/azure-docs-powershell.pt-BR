---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 672829daffa2117265e8f43b30f504adc702f3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772095"
---
# <span data-ttu-id="ae9f1-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae9f1-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ae9f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9f1-103">Adiciona um pool de NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="ae9f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae9f1-104">SYNTAX</span></span>

### <span data-ttu-id="ae9f1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae9f1-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9f1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae9f1-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9f1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae9f1-107">DESCRIPTION</span></span>
<span data-ttu-id="ae9f1-108">O cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** adiciona um pool de NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="ae9f1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae9f1-109">EXAMPLES</span></span>

### <span data-ttu-id="ae9f1-110">1: Adicionar</span><span class="sxs-lookup"><span data-stu-id="ae9f1-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="ae9f1-111">OS</span><span class="sxs-lookup"><span data-stu-id="ae9f1-111">PARAMETERS</span></span>

### <span data-ttu-id="ae9f1-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ae9f1-112">-BackendPort</span></span>
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

### <span data-ttu-id="ae9f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9f1-113">-DefaultProfile</span></span>
<span data-ttu-id="ae9f1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae9f1-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ae9f1-115">-EnableFloatingIP</span></span>
<span data-ttu-id="ae9f1-116">Configura o ponto de extremidade da máquina virtual para a funcionalidade de IP flutuante necessária para configurar um grupo de disponibilidade AlwaysOn do SQL.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="ae9f1-117">Essa configuração é necessária ao usar os grupos de disponibilidade AlwaysOn do SQL no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="ae9f1-118">Esta configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-118">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ae9f1-119">-EnableTcpReset</span></span>
<span data-ttu-id="ae9f1-120">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ae9f1-121">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-121">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae9f1-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ae9f1-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ae9f1-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="ae9f1-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="ae9f1-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="ae9f1-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ae9f1-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ae9f1-127">O tempo limite para a conexão TCP ociosa.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="ae9f1-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="ae9f1-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-129">The default value is 4 minutes.</span></span> <span data-ttu-id="ae9f1-130">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-130">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-131">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="ae9f1-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="ae9f1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae9f1-132">-Name</span></span>
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

### <span data-ttu-id="ae9f1-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="ae9f1-133">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae9f1-134">-Confirm</span></span>
<span data-ttu-id="ae9f1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9f1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9f1-136">-WhatIf</span></span>
<span data-ttu-id="ae9f1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae9f1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9f1-139">CommonParameters</span></span>
<span data-ttu-id="ae9f1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9f1-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae9f1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9f1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae9f1-142">INPUTS</span></span>

### <span data-ttu-id="ae9f1-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae9f1-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ae9f1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ae9f1-144">System.String</span></span>

### <span data-ttu-id="ae9f1-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ae9f1-145">System.Int32</span></span>

### <span data-ttu-id="ae9f1-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae9f1-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ae9f1-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae9f1-147">OUTPUTS</span></span>

### <span data-ttu-id="ae9f1-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae9f1-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae9f1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae9f1-149">NOTES</span></span>

## <span data-ttu-id="ae9f1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae9f1-150">RELATED LINKS</span></span>

[<span data-ttu-id="ae9f1-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae9f1-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ae9f1-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae9f1-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ae9f1-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae9f1-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ae9f1-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae9f1-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)