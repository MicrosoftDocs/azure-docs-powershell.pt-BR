---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 10539a09c8849f1afd5cd3c5bd9e249929577342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886873"
---
# <span data-ttu-id="8fe0b-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8fe0b-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8fe0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe0b-103">Define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8fe0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8fe0b-104">SYNTAX</span></span>

### <span data-ttu-id="8fe0b-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8fe0b-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fe0b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe0b-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fe0b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8fe0b-107">DESCRIPTION</span></span>
<span data-ttu-id="8fe0b-108">O cmdlet **Set-AzLoadBalancerInboundNatPoolConfig** define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8fe0b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-109">EXAMPLES</span></span>

### <span data-ttu-id="8fe0b-110">Exemplo 1: Definir</span><span class="sxs-lookup"><span data-stu-id="8fe0b-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="8fe0b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-111">PARAMETERS</span></span>

### <span data-ttu-id="8fe0b-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8fe0b-112">-BackendPort</span></span>
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

### <span data-ttu-id="8fe0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe0b-113">-DefaultProfile</span></span>
<span data-ttu-id="8fe0b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fe0b-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8fe0b-115">-EnableFloatingIP</span></span>
<span data-ttu-id="8fe0b-116">Configura o ponto de extremidade de uma máquina virtual para o recurso IP flutuante necessário para configurar um grupo de disponibilidade SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="8fe0b-117">Essa configuração é necessária ao usar o SQL Grupos de Disponibilidade AlwaysOn no SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="8fe0b-118">Essa configuração não pode ser alterada após a criação do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="8fe0b-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8fe0b-119">-EnableTcpReset</span></span>
<span data-ttu-id="8fe0b-120">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="8fe0b-121">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8fe0b-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe0b-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="8fe0b-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8fe0b-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="8fe0b-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="8fe0b-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="8fe0b-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="8fe0b-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="8fe0b-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8fe0b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8fe0b-127">O tempo de tempo para a conexão ociosa TCP.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="8fe0b-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="8fe0b-129">O valor padrão é 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-129">The default value is 4 minutes.</span></span> <span data-ttu-id="8fe0b-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8fe0b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fe0b-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="8fe0b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8fe0b-132">-Name</span></span>
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

### <span data-ttu-id="8fe0b-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8fe0b-133">-Protocol</span></span>
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

### <span data-ttu-id="8fe0b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fe0b-134">-Confirm</span></span>
<span data-ttu-id="8fe0b-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fe0b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fe0b-136">-WhatIf</span></span>
<span data-ttu-id="8fe0b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fe0b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fe0b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe0b-139">CommonParameters</span></span>
<span data-ttu-id="8fe0b-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe0b-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe0b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe0b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-142">INPUTS</span></span>

### <span data-ttu-id="8fe0b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fe0b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="8fe0b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe0b-144">System.String</span></span>

### <span data-ttu-id="8fe0b-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8fe0b-145">System.Int32</span></span>

### <span data-ttu-id="8fe0b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe0b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="8fe0b-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-147">OUTPUTS</span></span>

### <span data-ttu-id="8fe0b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8fe0b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8fe0b-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="8fe0b-149">NOTES</span></span>

## <span data-ttu-id="8fe0b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fe0b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8fe0b-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8fe0b-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8fe0b-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8fe0b-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8fe0b-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8fe0b-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8fe0b-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8fe0b-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
