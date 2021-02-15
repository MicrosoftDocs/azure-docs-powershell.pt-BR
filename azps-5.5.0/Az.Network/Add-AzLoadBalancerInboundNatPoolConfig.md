---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 993b1a3987427f096ecd061199663b35b6577b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115209"
---
# <span data-ttu-id="6636a-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6636a-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="6636a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6636a-102">SYNOPSIS</span></span>
<span data-ttu-id="6636a-103">Adiciona um pool NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6636a-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="6636a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6636a-104">SYNTAX</span></span>

### <span data-ttu-id="6636a-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6636a-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6636a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6636a-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6636a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6636a-107">DESCRIPTION</span></span>
<span data-ttu-id="6636a-108">O cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** adiciona um pool NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6636a-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="6636a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6636a-109">EXAMPLES</span></span>

### <span data-ttu-id="6636a-110">Exemplo 1: Adicionar</span><span class="sxs-lookup"><span data-stu-id="6636a-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="6636a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6636a-111">PARAMETERS</span></span>

### <span data-ttu-id="6636a-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6636a-112">-BackendPort</span></span>
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

### <span data-ttu-id="6636a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6636a-113">-DefaultProfile</span></span>
<span data-ttu-id="6636a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6636a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6636a-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="6636a-115">-EnableFloatingIP</span></span>
<span data-ttu-id="6636a-116">Configura o ponto de extremidade de uma máquina virtual para o recurso IP flutuante necessário para configurar um Grupo de Disponibilidade do SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="6636a-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="6636a-117">Essa configuração é necessária ao usar os Grupos de Disponibilidade do SQL AlwaysOn no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6636a-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="6636a-118">Essa configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6636a-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="6636a-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="6636a-119">-EnableTcpReset</span></span>
<span data-ttu-id="6636a-120">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="6636a-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6636a-121">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="6636a-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6636a-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6636a-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="6636a-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6636a-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="6636a-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="6636a-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="6636a-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="6636a-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="6636a-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6636a-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6636a-127">O tempo de tempo para a conexão Ociosa TCP.</span><span class="sxs-lookup"><span data-stu-id="6636a-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="6636a-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="6636a-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="6636a-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="6636a-129">The default value is 4 minutes.</span></span> <span data-ttu-id="6636a-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="6636a-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6636a-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6636a-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="6636a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6636a-132">-Name</span></span>
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

### <span data-ttu-id="6636a-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6636a-133">-Protocol</span></span>
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

### <span data-ttu-id="6636a-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6636a-134">-Confirm</span></span>
<span data-ttu-id="6636a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6636a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6636a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6636a-136">-WhatIf</span></span>
<span data-ttu-id="6636a-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6636a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6636a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6636a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6636a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6636a-139">CommonParameters</span></span>
<span data-ttu-id="6636a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6636a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6636a-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6636a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6636a-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="6636a-142">INPUTS</span></span>

### <span data-ttu-id="6636a-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6636a-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6636a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6636a-144">System.String</span></span>

### <span data-ttu-id="6636a-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6636a-145">System.Int32</span></span>

### <span data-ttu-id="6636a-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6636a-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="6636a-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="6636a-147">OUTPUTS</span></span>

### <span data-ttu-id="6636a-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6636a-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6636a-149">Notas</span><span class="sxs-lookup"><span data-stu-id="6636a-149">NOTES</span></span>

## <span data-ttu-id="6636a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6636a-150">RELATED LINKS</span></span>

[<span data-ttu-id="6636a-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6636a-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6636a-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6636a-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6636a-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6636a-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="6636a-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6636a-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
