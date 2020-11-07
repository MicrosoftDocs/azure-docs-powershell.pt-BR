---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945733"
---
# <span data-ttu-id="1d94c-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d94c-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="1d94c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d94c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d94c-103">Adiciona um ponto de extremidade a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d94c-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="1d94c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d94c-104">SYNTAX</span></span>

### <span data-ttu-id="1d94c-105">NoLB (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d94c-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1d94c-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="1d94c-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1d94c-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="1d94c-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1d94c-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="1d94c-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d94c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d94c-109">DESCRIPTION</span></span>
<span data-ttu-id="1d94c-110">O cmdlet **Add-AzureEndpoint** adiciona um ponto de extremidade a um objeto de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d94c-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="1d94c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d94c-111">EXAMPLES</span></span>

### <span data-ttu-id="1d94c-112">Exemplo 1: adicionar um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="1d94c-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="1d94c-113">Esse comando recupera a configuração de uma máquina virtual nomeada VirtualMachine01 usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1d94c-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="1d94c-114">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d94c-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d94c-115">Esse cmdlet adiciona um ponto de extremidade chamado Httpem.</span><span class="sxs-lookup"><span data-stu-id="1d94c-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1d94c-116">O ponto de extremidade tem uma porta pública 80 e a porta local 8080.</span><span class="sxs-lookup"><span data-stu-id="1d94c-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1d94c-117">O comando passa o objeto da máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="1d94c-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="1d94c-118">Exemplo 2: adicionar um ponto de extremidade que pertence a um grupo com balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="1d94c-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="1d94c-119">Esse comando recupera a configuração de uma máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="1d94c-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1d94c-120">O cmdlet atual adiciona um ponto de extremidade chamado Httpem.</span><span class="sxs-lookup"><span data-stu-id="1d94c-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1d94c-121">O ponto de extremidade tem uma porta pública 80 e a porta local 8080.</span><span class="sxs-lookup"><span data-stu-id="1d94c-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1d94c-122">O ponto de extremidade pertence ao grupo de balanceamento de carga compartilhado chamado WebFarm.</span><span class="sxs-lookup"><span data-stu-id="1d94c-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="1d94c-123">Um teste HTTP na porta 80 com um caminho de '/' monitora a disponibilidade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="1d94c-124">O comando implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="1d94c-124">The command implements your changes.</span></span>

### <span data-ttu-id="1d94c-125">Exemplo 3: associar um IP virtual a um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="1d94c-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="1d94c-126">Esse comando recupera a configuração de uma máquina virtual chamada VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="1d94c-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="1d94c-127">O cmdlet atual adiciona um ponto de extremidade chamado Httpem.</span><span class="sxs-lookup"><span data-stu-id="1d94c-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1d94c-128">O ponto de extremidade tem uma porta pública 80 e a porta local 8080.</span><span class="sxs-lookup"><span data-stu-id="1d94c-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1d94c-129">Esse comando associa um IP virtual ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="1d94c-130">O comando implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="1d94c-130">The command implements your changes.</span></span>

## <span data-ttu-id="1d94c-131">OS</span><span class="sxs-lookup"><span data-stu-id="1d94c-131">PARAMETERS</span></span>

### <span data-ttu-id="1d94c-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="1d94c-132">-ACL</span></span>
<span data-ttu-id="1d94c-133">Especifica um objeto de configuração de ACL (lista de controle de acesso) para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-134">-Defaultprobe</span><span class="sxs-lookup"><span data-stu-id="1d94c-134">-DefaultProbe</span></span>
<span data-ttu-id="1d94c-135">Indica que esse cmdlet usa a configuração padrão de teste.</span><span class="sxs-lookup"><span data-stu-id="1d94c-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="1d94c-136">-DirectServerReturn</span></span>
<span data-ttu-id="1d94c-137">Especifica se esse cmdlet habilita o retorno direto do servidor.</span><span class="sxs-lookup"><span data-stu-id="1d94c-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="1d94c-138">Especifique $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="1d94c-138">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1d94c-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1d94c-140">Especifica o período de tempo limite de ociosidade de TCP, em minutos, para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-141">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1d94c-141">-InformationAction</span></span>
<span data-ttu-id="1d94c-142">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="1d94c-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1d94c-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1d94c-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d94c-144">Contínuo</span><span class="sxs-lookup"><span data-stu-id="1d94c-144">Continue</span></span>
- <span data-ttu-id="1d94c-145">Ignorar</span><span class="sxs-lookup"><span data-stu-id="1d94c-145">Ignore</span></span>
- <span data-ttu-id="1d94c-146">Inquire</span><span class="sxs-lookup"><span data-stu-id="1d94c-146">Inquire</span></span>
- <span data-ttu-id="1d94c-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1d94c-147">SilentlyContinue</span></span>
- <span data-ttu-id="1d94c-148">Finaliza</span><span class="sxs-lookup"><span data-stu-id="1d94c-148">Stop</span></span>
- <span data-ttu-id="1d94c-149">Suspensão</span><span class="sxs-lookup"><span data-stu-id="1d94c-149">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1d94c-150">-InformationVariable</span></span>
<span data-ttu-id="1d94c-151">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="1d94c-151">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="1d94c-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="1d94c-153">Especifica o nome do balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="1d94c-153">Specifies the name of the internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="1d94c-154">-LBSetName</span></span>
<span data-ttu-id="1d94c-155">Especifica o nome do balanceador de carga definido para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="1d94c-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="1d94c-157">Especifica o algoritmo de distribuição do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1d94c-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="1d94c-158">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1d94c-158">Valid values are:</span></span> 

- <span data-ttu-id="1d94c-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="1d94c-159">sourceIP.</span></span>
<span data-ttu-id="1d94c-160">Uma afinidade de duas tuplas: IP de origem, IP de destino</span><span class="sxs-lookup"><span data-stu-id="1d94c-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="1d94c-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="1d94c-161">sourceIPProtocol.</span></span>
<span data-ttu-id="1d94c-162">Uma afinidade de três tupla: IP de origem, IP de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="1d94c-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="1d94c-163">nenhuma.</span><span class="sxs-lookup"><span data-stu-id="1d94c-163">none.</span></span>
<span data-ttu-id="1d94c-164">Uma afinidade de cinco tuplas: IP de origem, porta de origem, IP de destino, porta de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="1d94c-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="1d94c-165">O valor padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="1d94c-165">The default value is none.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="1d94c-166">-LocalPort</span></span>
<span data-ttu-id="1d94c-167">Especifica a porta local, privada, que este ponto de extremidade usa.</span><span class="sxs-lookup"><span data-stu-id="1d94c-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="1d94c-168">Os aplicativos na máquina virtual escutam nesta porta solicitações de entrada de serviço para este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d94c-169">-Name</span></span>
<span data-ttu-id="1d94c-170">Especifica um nome para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-171">-Noprobe</span><span class="sxs-lookup"><span data-stu-id="1d94c-171">-NoProbe</span></span>
<span data-ttu-id="1d94c-172">Indica que esse cmdlet usa a configuração sem sondagem.</span><span class="sxs-lookup"><span data-stu-id="1d94c-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d94c-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="1d94c-174">Especifica o intervalo de sondagem de sondagem, em segundos, para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="1d94c-175">-ProbePath</span></span>
<span data-ttu-id="1d94c-176">Especifica o caminho relativo para o teste HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d94c-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="1d94c-177">-ProbePort</span></span>
<span data-ttu-id="1d94c-178">Especifica a porta que o ponto de extremidade usa.</span><span class="sxs-lookup"><span data-stu-id="1d94c-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="1d94c-179">-ProbeProtocol</span></span>
<span data-ttu-id="1d94c-180">Especifica o protocolo de porta.</span><span class="sxs-lookup"><span data-stu-id="1d94c-180">Specifies the port protocol.</span></span>
<span data-ttu-id="1d94c-181">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1d94c-181">Valid values are:</span></span> 

- <span data-ttu-id="1d94c-182">Protocol</span><span class="sxs-lookup"><span data-stu-id="1d94c-182">tcp</span></span> 
- <span data-ttu-id="1d94c-183">http</span><span class="sxs-lookup"><span data-stu-id="1d94c-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d94c-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="1d94c-185">Especifica o período de tempo limite da sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="1d94c-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-186">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1d94c-186">-Profile</span></span>
<span data-ttu-id="1d94c-187">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1d94c-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d94c-188">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1d94c-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-189">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="1d94c-189">-Protocol</span></span>
<span data-ttu-id="1d94c-190">Especifica o protocolo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="1d94c-191">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1d94c-191">Valid values are:</span></span> 

- <span data-ttu-id="1d94c-192">Protocol</span><span class="sxs-lookup"><span data-stu-id="1d94c-192">tcp</span></span> 
- <span data-ttu-id="1d94c-193">grama</span><span class="sxs-lookup"><span data-stu-id="1d94c-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="1d94c-194">-PublicPort</span></span>
<span data-ttu-id="1d94c-195">Especifica a porta pública usada pelo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="1d94c-196">Se você não especificar um valor, o Azure atribuirá uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="1d94c-196">If you do not specify a value, Azure assigns an available port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1d94c-197">-VirtualIPName</span></span>
<span data-ttu-id="1d94c-198">Especifica o nome de um endereço IP virtual que o Azure associa ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="1d94c-199">Seu serviço pode ter vários IPs virtuais.</span><span class="sxs-lookup"><span data-stu-id="1d94c-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="1d94c-200">Para criar IPs virtuais, use o cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="1d94c-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-201">-VM</span><span class="sxs-lookup"><span data-stu-id="1d94c-201">-VM</span></span>
<span data-ttu-id="1d94c-202">Especifica a máquina virtual à qual pertence o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1d94c-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d94c-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d94c-203">CommonParameters</span></span>
<span data-ttu-id="1d94c-204">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d94c-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d94c-205">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d94c-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d94c-206">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d94c-206">INPUTS</span></span>

## <span data-ttu-id="1d94c-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d94c-207">OUTPUTS</span></span>

### <span data-ttu-id="1d94c-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="1d94c-208">System.Object</span></span>

## <span data-ttu-id="1d94c-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d94c-209">NOTES</span></span>

## <span data-ttu-id="1d94c-210">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d94c-210">RELATED LINKS</span></span>

[<span data-ttu-id="1d94c-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1d94c-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="1d94c-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d94c-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="1d94c-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1d94c-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1d94c-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d94c-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="1d94c-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d94c-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="1d94c-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1d94c-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


