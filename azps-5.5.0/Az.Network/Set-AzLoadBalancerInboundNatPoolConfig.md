---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115062"
---
# <span data-ttu-id="55b71-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55b71-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="55b71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55b71-102">SYNOPSIS</span></span>
<span data-ttu-id="55b71-103">Define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55b71-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="55b71-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55b71-104">SYNTAX</span></span>

### <span data-ttu-id="55b71-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55b71-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55b71-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55b71-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b71-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55b71-107">DESCRIPTION</span></span>
<span data-ttu-id="55b71-108">O cmdlet **Set-AzLoadBalancerInboundNatPoolConfig** define uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="55b71-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="55b71-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55b71-109">EXAMPLES</span></span>

### <span data-ttu-id="55b71-110">Exemplo 1: Definir</span><span class="sxs-lookup"><span data-stu-id="55b71-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="55b71-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55b71-111">PARAMETERS</span></span>

### <span data-ttu-id="55b71-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="55b71-112">-BackendPort</span></span>
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

### <span data-ttu-id="55b71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b71-113">-DefaultProfile</span></span>
<span data-ttu-id="55b71-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="55b71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b71-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="55b71-115">-EnableFloatingIP</span></span>
<span data-ttu-id="55b71-116">Configura o ponto de extremidade de uma máquina virtual para o recurso IP flutuante necessário para configurar um Grupo de Disponibilidade do SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="55b71-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="55b71-117">Essa configuração é necessária ao usar os Grupos de Disponibilidade do SQL AlwaysOn no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="55b71-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="55b71-118">Essa configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="55b71-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="55b71-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="55b71-119">-EnableTcpReset</span></span>
<span data-ttu-id="55b71-120">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="55b71-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="55b71-121">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="55b71-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="55b71-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="55b71-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="55b71-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="55b71-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="55b71-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="55b71-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="55b71-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="55b71-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="55b71-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="55b71-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="55b71-127">O tempo de tempo para a conexão Ociosa TCP.</span><span class="sxs-lookup"><span data-stu-id="55b71-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="55b71-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="55b71-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="55b71-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="55b71-129">The default value is 4 minutes.</span></span> <span data-ttu-id="55b71-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="55b71-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="55b71-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55b71-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="55b71-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="55b71-132">-Name</span></span>
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

### <span data-ttu-id="55b71-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="55b71-133">-Protocol</span></span>
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

### <span data-ttu-id="55b71-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55b71-134">-Confirm</span></span>
<span data-ttu-id="55b71-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b71-136">-WhatIf</span></span>
<span data-ttu-id="55b71-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55b71-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55b71-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55b71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b71-139">CommonParameters</span></span>
<span data-ttu-id="55b71-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b71-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b71-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b71-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="55b71-142">INPUTS</span></span>

### <span data-ttu-id="55b71-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55b71-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="55b71-144">System.String</span><span class="sxs-lookup"><span data-stu-id="55b71-144">System.String</span></span>

### <span data-ttu-id="55b71-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="55b71-145">System.Int32</span></span>

### <span data-ttu-id="55b71-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55b71-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="55b71-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="55b71-147">OUTPUTS</span></span>

### <span data-ttu-id="55b71-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55b71-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55b71-149">Notas</span><span class="sxs-lookup"><span data-stu-id="55b71-149">NOTES</span></span>

## <span data-ttu-id="55b71-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55b71-150">RELATED LINKS</span></span>

[<span data-ttu-id="55b71-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55b71-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55b71-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55b71-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55b71-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55b71-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55b71-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55b71-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
