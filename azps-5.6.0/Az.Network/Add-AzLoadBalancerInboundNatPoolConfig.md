---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 58ee0531ea0671314e6f1e6d590b388c3f82ef34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889194"
---
# <span data-ttu-id="e0035-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0035-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e0035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0035-102">SYNOPSIS</span></span>
<span data-ttu-id="e0035-103">Adiciona um pool NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e0035-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="e0035-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e0035-104">SYNTAX</span></span>

### <span data-ttu-id="e0035-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0035-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0035-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0035-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0035-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e0035-107">DESCRIPTION</span></span>
<span data-ttu-id="e0035-108">O cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** adiciona um pool NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e0035-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="e0035-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0035-109">EXAMPLES</span></span>

### <span data-ttu-id="e0035-110">Exemplo 1: Adicionar</span><span class="sxs-lookup"><span data-stu-id="e0035-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
PS C:\> $lb | Set-AzLoadBalancer
```

## <span data-ttu-id="e0035-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e0035-111">PARAMETERS</span></span>

### <span data-ttu-id="e0035-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e0035-112">-BackendPort</span></span>
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

### <span data-ttu-id="e0035-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0035-113">-DefaultProfile</span></span>
<span data-ttu-id="e0035-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e0035-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0035-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="e0035-115">-EnableFloatingIP</span></span>
<span data-ttu-id="e0035-116">Configura o ponto de extremidade de uma máquina virtual para o recurso IP flutuante necessário para configurar um grupo de disponibilidade SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="e0035-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="e0035-117">Essa configuração é necessária ao usar o SQL Grupos de Disponibilidade AlwaysOn no SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="e0035-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="e0035-118">Essa configuração não pode ser alterada após a criação do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e0035-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="e0035-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e0035-119">-EnableTcpReset</span></span>
<span data-ttu-id="e0035-120">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="e0035-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="e0035-121">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="e0035-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e0035-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0035-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="e0035-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e0035-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="e0035-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="e0035-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="e0035-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="e0035-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="e0035-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e0035-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e0035-127">O tempo de tempo para a conexão ociosa TCP.</span><span class="sxs-lookup"><span data-stu-id="e0035-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="e0035-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e0035-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="e0035-129">O valor padrão é 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="e0035-129">The default value is 4 minutes.</span></span> <span data-ttu-id="e0035-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="e0035-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e0035-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0035-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="e0035-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e0035-132">-Name</span></span>
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

### <span data-ttu-id="e0035-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e0035-133">-Protocol</span></span>
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

### <span data-ttu-id="e0035-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0035-134">-Confirm</span></span>
<span data-ttu-id="e0035-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0035-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0035-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0035-136">-WhatIf</span></span>
<span data-ttu-id="e0035-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0035-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0035-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0035-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0035-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0035-139">CommonParameters</span></span>
<span data-ttu-id="e0035-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0035-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0035-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0035-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0035-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0035-142">INPUTS</span></span>

### <span data-ttu-id="e0035-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0035-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e0035-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e0035-144">System.String</span></span>

### <span data-ttu-id="e0035-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e0035-145">System.Int32</span></span>

### <span data-ttu-id="e0035-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0035-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e0035-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e0035-147">OUTPUTS</span></span>

### <span data-ttu-id="e0035-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0035-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e0035-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="e0035-149">NOTES</span></span>

## <span data-ttu-id="e0035-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0035-150">RELATED LINKS</span></span>

[<span data-ttu-id="e0035-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0035-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e0035-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0035-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e0035-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0035-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e0035-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0035-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
