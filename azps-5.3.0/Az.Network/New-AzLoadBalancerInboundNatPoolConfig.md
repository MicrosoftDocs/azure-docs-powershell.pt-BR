---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427578"
---
# <span data-ttu-id="c7719-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7719-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c7719-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7719-102">SYNOPSIS</span></span>
<span data-ttu-id="c7719-103">Cria uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c7719-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c7719-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7719-104">SYNTAX</span></span>

### <span data-ttu-id="c7719-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7719-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7719-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7719-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7719-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7719-107">DESCRIPTION</span></span>
<span data-ttu-id="c7719-108">O cmdlet **New-AzLoadBalancerInboundNatPoolConfig** cria uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="c7719-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c7719-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7719-109">EXAMPLES</span></span>

### <span data-ttu-id="c7719-110">Exemplo 1: novo</span><span class="sxs-lookup"><span data-stu-id="c7719-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="c7719-111">OS</span><span class="sxs-lookup"><span data-stu-id="c7719-111">PARAMETERS</span></span>

### <span data-ttu-id="c7719-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c7719-112">-BackendPort</span></span>
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

### <span data-ttu-id="c7719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7719-113">-DefaultProfile</span></span>
<span data-ttu-id="c7719-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7719-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7719-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c7719-115">-EnableFloatingIP</span></span>
<span data-ttu-id="c7719-116">Configura o ponto de extremidade da máquina virtual para a funcionalidade de IP flutuante necessária para configurar um grupo de disponibilidade AlwaysOn do SQL.</span><span class="sxs-lookup"><span data-stu-id="c7719-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="c7719-117">Essa configuração é necessária ao usar os grupos de disponibilidade AlwaysOn do SQL no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7719-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="c7719-118">Esta configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7719-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="c7719-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c7719-119">-EnableTcpReset</span></span>
<span data-ttu-id="c7719-120">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="c7719-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c7719-121">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="c7719-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c7719-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7719-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="c7719-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7719-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="c7719-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c7719-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="c7719-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c7719-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="c7719-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c7719-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c7719-127">O tempo limite para a conexão TCP ociosa.</span><span class="sxs-lookup"><span data-stu-id="c7719-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="c7719-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="c7719-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="c7719-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="c7719-129">The default value is 4 minutes.</span></span> <span data-ttu-id="c7719-130">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="c7719-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c7719-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7719-131">-Name</span></span>
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

### <span data-ttu-id="c7719-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="c7719-132">-Protocol</span></span>
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

### <span data-ttu-id="c7719-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7719-133">-Confirm</span></span>
<span data-ttu-id="c7719-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7719-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7719-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7719-135">-WhatIf</span></span>
<span data-ttu-id="c7719-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7719-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7719-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7719-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7719-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7719-138">CommonParameters</span></span>
<span data-ttu-id="c7719-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7719-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7719-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7719-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7719-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7719-141">INPUTS</span></span>

### <span data-ttu-id="c7719-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c7719-142">System.String</span></span>

### <span data-ttu-id="c7719-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c7719-143">System.Int32</span></span>

### <span data-ttu-id="c7719-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7719-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c7719-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7719-145">OUTPUTS</span></span>

### <span data-ttu-id="c7719-146">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c7719-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c7719-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7719-147">NOTES</span></span>

## <span data-ttu-id="c7719-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7719-148">RELATED LINKS</span></span>

[<span data-ttu-id="c7719-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7719-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7719-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7719-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7719-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7719-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7719-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7719-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
