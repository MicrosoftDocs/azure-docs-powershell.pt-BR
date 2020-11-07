---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945953"
---
# <span data-ttu-id="56c8f-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="56c8f-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="56c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="56c8f-103">Modifica todos os pontos de extremidade em um balanceador de carga definido dentro de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="56c8f-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="56c8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56c8f-104">SYNTAX</span></span>

### <span data-ttu-id="56c8f-105">Defaultprobe (padrão)</span><span class="sxs-lookup"><span data-stu-id="56c8f-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="56c8f-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="56c8f-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="56c8f-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="56c8f-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56c8f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56c8f-108">DESCRIPTION</span></span>
<span data-ttu-id="56c8f-109">O cmdlet **set-AzureLoadBalancedEndpoint** modifica todos os pontos de extremidade em um balanceador de carga definido em um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="56c8f-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="56c8f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56c8f-110">EXAMPLES</span></span>

### <span data-ttu-id="56c8f-111">Exemplo 1: modificar os pontos de extremidade em um conjunto de balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="56c8f-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="56c8f-112">Esse comando modifica todos os pontos de extremidade no conjunto de balanceamento de carga chamado LBSet01 para usar o protocolo TCP e a porta privada 80.</span><span class="sxs-lookup"><span data-stu-id="56c8f-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="56c8f-113">O comando define o teste de balanceador de carga para usar o protocolo TCP na porta 8080.</span><span class="sxs-lookup"><span data-stu-id="56c8f-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="56c8f-114">Exemplo 2: especificar um IP virtual diferente</span><span class="sxs-lookup"><span data-stu-id="56c8f-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="56c8f-115">Esse comando modifica o balanceador de carga que tem o nome do conjunto de balanceamento de carga para usar um IP virtual chamado Vip01.</span><span class="sxs-lookup"><span data-stu-id="56c8f-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="56c8f-116">OS</span><span class="sxs-lookup"><span data-stu-id="56c8f-116">PARAMETERS</span></span>

### <span data-ttu-id="56c8f-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="56c8f-117">-ACL</span></span>
<span data-ttu-id="56c8f-118">Especifica um objeto de configuração de ACL (lista de controle de acesso) que esse cmdlet aplica aos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

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

### <span data-ttu-id="56c8f-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="56c8f-119">-DirectServerReturn</span></span>
<span data-ttu-id="56c8f-120">Especifica se esse cmdlet habilita o retorno direto do servidor.</span><span class="sxs-lookup"><span data-stu-id="56c8f-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="56c8f-121">Especifique $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="56c8f-121">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="56c8f-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="56c8f-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="56c8f-123">Especifica o período de tempo limite de ociosidade de TCP, em minutos, para os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="56c8f-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="56c8f-124">-InformationAction</span></span>
<span data-ttu-id="56c8f-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="56c8f-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56c8f-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="56c8f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56c8f-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="56c8f-127">Continue</span></span>
- <span data-ttu-id="56c8f-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="56c8f-128">Ignore</span></span>
- <span data-ttu-id="56c8f-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="56c8f-129">Inquire</span></span>
- <span data-ttu-id="56c8f-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56c8f-130">SilentlyContinue</span></span>
- <span data-ttu-id="56c8f-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="56c8f-131">Stop</span></span>
- <span data-ttu-id="56c8f-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="56c8f-132">Suspend</span></span>

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

### <span data-ttu-id="56c8f-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56c8f-133">-InformationVariable</span></span>
<span data-ttu-id="56c8f-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="56c8f-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56c8f-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="56c8f-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="56c8f-136">Especifica o nome do balanceador de carga interno que este cmdlet inclui na configuração.</span><span class="sxs-lookup"><span data-stu-id="56c8f-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="56c8f-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="56c8f-137">-LBSetName</span></span>
<span data-ttu-id="56c8f-138">Especifica o nome do conjunto de balanceador de carga que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="56c8f-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="56c8f-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="56c8f-140">Especifica o algoritmo de distribuição do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="56c8f-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="56c8f-141">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="56c8f-141">Valid values are:</span></span> 

- <span data-ttu-id="56c8f-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="56c8f-142">sourceIP.</span></span>
<span data-ttu-id="56c8f-143">Uma afinidade de duas tuplas: IP de origem, IP de destino</span><span class="sxs-lookup"><span data-stu-id="56c8f-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="56c8f-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="56c8f-144">sourceIPProtocol.</span></span>
<span data-ttu-id="56c8f-145">Uma afinidade de três tupla: IP de origem, IP de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="56c8f-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="56c8f-146">nenhuma.</span><span class="sxs-lookup"><span data-stu-id="56c8f-146">none.</span></span>
<span data-ttu-id="56c8f-147">Uma afinidade de cinco tuplas: IP de origem, porta de origem, IP de destino, porta de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="56c8f-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="56c8f-148">O valor padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="56c8f-148">The default value is none.</span></span>

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

### <span data-ttu-id="56c8f-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="56c8f-149">-LocalPort</span></span>
<span data-ttu-id="56c8f-150">Especifica a porta local, privada, que esses pontos de extremidade usam.</span><span class="sxs-lookup"><span data-stu-id="56c8f-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="56c8f-151">Os aplicativos na máquina virtual escutam nesta porta solicitações de entrada de serviço para este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="56c8f-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="56c8f-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="56c8f-153">Especifica o intervalo de sondagem de sondagem, em segundos, para os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="56c8f-154">-ProbePath</span></span>
<span data-ttu-id="56c8f-155">Especifica o caminho relativo do teste HTTP.</span><span class="sxs-lookup"><span data-stu-id="56c8f-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="56c8f-156">-ProbePort</span></span>
<span data-ttu-id="56c8f-157">Especifica a porta que a sonda do balanceador de carga usa.</span><span class="sxs-lookup"><span data-stu-id="56c8f-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="56c8f-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="56c8f-159">Especifica que os pontos de extremidade do balanceador de carga usam uma investigação HTTP.</span><span class="sxs-lookup"><span data-stu-id="56c8f-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="56c8f-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="56c8f-161">Especifica que os pontos de extremidade do balanceador de carga usam um teste TCP.</span><span class="sxs-lookup"><span data-stu-id="56c8f-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="56c8f-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="56c8f-163">Especifica o tempo limite de sondagem de teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="56c8f-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-164">-Perfil</span><span class="sxs-lookup"><span data-stu-id="56c8f-164">-Profile</span></span>
<span data-ttu-id="56c8f-165">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="56c8f-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56c8f-166">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="56c8f-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56c8f-167">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="56c8f-167">-Protocol</span></span>
<span data-ttu-id="56c8f-168">Especifica o protocolo dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="56c8f-169">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="56c8f-169">Valid values are:</span></span> 

- <span data-ttu-id="56c8f-170">Protocol</span><span class="sxs-lookup"><span data-stu-id="56c8f-170">TCP</span></span> 
- <span data-ttu-id="56c8f-171">GRAMA</span><span class="sxs-lookup"><span data-stu-id="56c8f-171">UDP</span></span>

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

### <span data-ttu-id="56c8f-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="56c8f-172">-PublicPort</span></span>
<span data-ttu-id="56c8f-173">Especifica a porta pública usada pelo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="56c8f-174">Se você não especificar um valor, o Azure atribuirá uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="56c8f-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="56c8f-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56c8f-175">-ServiceName</span></span>
<span data-ttu-id="56c8f-176">Especifica o nome do serviço do Azure que contém os pontos de extremidade que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="56c8f-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c8f-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="56c8f-177">-VirtualIPName</span></span>
<span data-ttu-id="56c8f-178">Especifica o nome de um endereço IP virtual que o Azure associa a pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="56c8f-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="56c8f-179">Para adicionar o IPs virtual ao seu serviço, use o cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="56c8f-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="56c8f-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c8f-180">CommonParameters</span></span>
<span data-ttu-id="56c8f-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c8f-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c8f-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c8f-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c8f-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56c8f-183">INPUTS</span></span>

## <span data-ttu-id="56c8f-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56c8f-184">OUTPUTS</span></span>

## <span data-ttu-id="56c8f-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56c8f-185">NOTES</span></span>

## <span data-ttu-id="56c8f-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56c8f-186">RELATED LINKS</span></span>

[<span data-ttu-id="56c8f-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="56c8f-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="56c8f-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56c8f-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


