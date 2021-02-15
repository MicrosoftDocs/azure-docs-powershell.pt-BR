---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111627"
---
# <span data-ttu-id="abc74-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="abc74-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="abc74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abc74-102">SYNOPSIS</span></span>
<span data-ttu-id="abc74-103">Cria uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="abc74-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="abc74-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abc74-104">SYNTAX</span></span>

### <span data-ttu-id="abc74-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="abc74-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc74-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="abc74-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc74-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="abc74-107">DESCRIPTION</span></span>
<span data-ttu-id="abc74-108">O **cmdlet New-AzLoadBalancerInboundNatPoolConfig** cria uma configuração de pool NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="abc74-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="abc74-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="abc74-109">EXAMPLES</span></span>

### <span data-ttu-id="abc74-110">Exemplo 1: Novo</span><span class="sxs-lookup"><span data-stu-id="abc74-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="abc74-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abc74-111">PARAMETERS</span></span>

### <span data-ttu-id="abc74-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="abc74-112">-BackendPort</span></span>
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

### <span data-ttu-id="abc74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc74-113">-DefaultProfile</span></span>
<span data-ttu-id="abc74-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="abc74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc74-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="abc74-115">-EnableFloatingIP</span></span>
<span data-ttu-id="abc74-116">Configura o ponto de extremidade de uma máquina virtual para o recurso IP flutuante necessário para configurar um Grupo de Disponibilidade do SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="abc74-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="abc74-117">Essa configuração é necessária ao usar os Grupos de Disponibilidade do SQL AlwaysOn no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abc74-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="abc74-118">Essa configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="abc74-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="abc74-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="abc74-119">-EnableTcpReset</span></span>
<span data-ttu-id="abc74-120">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="abc74-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="abc74-121">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="abc74-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="abc74-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="abc74-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="abc74-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="abc74-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="abc74-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="abc74-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="abc74-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="abc74-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="abc74-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="abc74-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="abc74-127">O tempo de tempo para a conexão Ociosa TCP.</span><span class="sxs-lookup"><span data-stu-id="abc74-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="abc74-128">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="abc74-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="abc74-129">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="abc74-129">The default value is 4 minutes.</span></span> <span data-ttu-id="abc74-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="abc74-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="abc74-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="abc74-131">-Name</span></span>
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

### <span data-ttu-id="abc74-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="abc74-132">-Protocol</span></span>
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

### <span data-ttu-id="abc74-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="abc74-133">-Confirm</span></span>
<span data-ttu-id="abc74-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc74-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc74-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc74-135">-WhatIf</span></span>
<span data-ttu-id="abc74-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="abc74-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abc74-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abc74-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc74-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc74-138">CommonParameters</span></span>
<span data-ttu-id="abc74-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc74-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc74-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc74-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc74-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="abc74-141">INPUTS</span></span>

### <span data-ttu-id="abc74-142">System.String</span><span class="sxs-lookup"><span data-stu-id="abc74-142">System.String</span></span>

### <span data-ttu-id="abc74-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="abc74-143">System.Int32</span></span>

### <span data-ttu-id="abc74-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="abc74-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="abc74-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="abc74-145">OUTPUTS</span></span>

### <span data-ttu-id="abc74-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="abc74-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="abc74-147">Notas</span><span class="sxs-lookup"><span data-stu-id="abc74-147">NOTES</span></span>

## <span data-ttu-id="abc74-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abc74-148">RELATED LINKS</span></span>

[<span data-ttu-id="abc74-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="abc74-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="abc74-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="abc74-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="abc74-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="abc74-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="abc74-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="abc74-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
