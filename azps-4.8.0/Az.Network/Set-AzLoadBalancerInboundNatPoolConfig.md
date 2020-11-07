---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954778"
---
# <span data-ttu-id="9ec89-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9ec89-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9ec89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ec89-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec89-103">Define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="9ec89-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="9ec89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ec89-104">SYNTAX</span></span>

### <span data-ttu-id="9ec89-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ec89-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec89-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec89-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec89-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ec89-107">DESCRIPTION</span></span>
<span data-ttu-id="9ec89-108">O cmdlet **set-AzLoadBalancerInboundNatPoolConfig** define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="9ec89-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="9ec89-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ec89-109">EXAMPLES</span></span>

### <span data-ttu-id="9ec89-110">Exemplo 1: definir</span><span class="sxs-lookup"><span data-stu-id="9ec89-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="9ec89-111">OS</span><span class="sxs-lookup"><span data-stu-id="9ec89-111">PARAMETERS</span></span>

### <span data-ttu-id="9ec89-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9ec89-112">-BackendPort</span></span>
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

### <span data-ttu-id="9ec89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec89-113">-DefaultProfile</span></span>
<span data-ttu-id="9ec89-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ec89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ec89-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9ec89-115">-EnableFloatingIP</span></span>
<span data-ttu-id="9ec89-116">Configura o ponto de extremidade da máquina virtual para a funcionalidade de IP flutuante necessária para configurar um grupo de disponibilidade AlwaysOn do SQL.</span><span class="sxs-lookup"><span data-stu-id="9ec89-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="9ec89-117">Essa configuração é necessária ao usar os grupos de disponibilidade AlwaysOn do SQL no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ec89-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="9ec89-118">Esta configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9ec89-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="9ec89-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9ec89-119">-EnableTcpReset</span></span>
<span data-ttu-id="9ec89-120">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="9ec89-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9ec89-121">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="9ec89-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9ec89-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ec89-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="9ec89-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9ec89-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="9ec89-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="9ec89-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="9ec89-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="9ec89-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="9ec89-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9ec89-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9ec89-127">O tempo limite para a conexão TCP ociosa.</span><span class="sxs-lookup"><span data-stu-id="9ec89-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="9ec89-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="9ec89-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="9ec89-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="9ec89-129">The default value is 4 minutes.</span></span> <span data-ttu-id="9ec89-130">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="9ec89-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9ec89-131">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="9ec89-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="9ec89-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ec89-132">-Name</span></span>
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

### <span data-ttu-id="9ec89-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="9ec89-133">-Protocol</span></span>
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

### <span data-ttu-id="9ec89-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ec89-134">-Confirm</span></span>
<span data-ttu-id="9ec89-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec89-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec89-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec89-136">-WhatIf</span></span>
<span data-ttu-id="9ec89-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ec89-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ec89-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ec89-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec89-139">CommonParameters</span></span>
<span data-ttu-id="9ec89-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec89-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec89-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec89-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ec89-142">INPUTS</span></span>

### <span data-ttu-id="9ec89-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9ec89-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9ec89-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9ec89-144">System.String</span></span>

### <span data-ttu-id="9ec89-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9ec89-145">System.Int32</span></span>

### <span data-ttu-id="9ec89-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ec89-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9ec89-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ec89-147">OUTPUTS</span></span>

### <span data-ttu-id="9ec89-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9ec89-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9ec89-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ec89-149">NOTES</span></span>

## <span data-ttu-id="9ec89-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ec89-150">RELATED LINKS</span></span>

[<span data-ttu-id="9ec89-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9ec89-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9ec89-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9ec89-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9ec89-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9ec89-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="9ec89-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9ec89-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
