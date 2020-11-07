---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946057"
---
# <span data-ttu-id="a46af-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a46af-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="a46af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a46af-102">SYNOPSIS</span></span>
<span data-ttu-id="a46af-103">Modifica um ponto de extremidade atribuído a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a46af-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="a46af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a46af-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a46af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a46af-105">DESCRIPTION</span></span>
<span data-ttu-id="a46af-106">O cmdlet **set-AzureEndpoint** modifica um ponto de extremidade atribuído a uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a46af-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="a46af-107">Você pode especificar alterações em um ponto de extremidade cuja carga não seja balanceada.</span><span class="sxs-lookup"><span data-stu-id="a46af-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="a46af-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a46af-108">EXAMPLES</span></span>

### <span data-ttu-id="a46af-109">Exemplo 1: modificar um ponto de extremidade para escutar em uma porta</span><span class="sxs-lookup"><span data-stu-id="a46af-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="a46af-110">Esse comando recupera a configuração de uma máquina virtual nomeada VirtualMachine01 usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a46af-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a46af-111">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a46af-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a46af-112">Esse cmdlet modifica o ponto de extremidade chamado Web para escuta na porta 443.</span><span class="sxs-lookup"><span data-stu-id="a46af-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="a46af-113">O comando passa o objeto da máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="a46af-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="a46af-114">OS</span><span class="sxs-lookup"><span data-stu-id="a46af-114">PARAMETERS</span></span>

### <span data-ttu-id="a46af-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="a46af-115">-ACL</span></span>
<span data-ttu-id="a46af-116">Especifica um objeto de configuração de ACL (lista de controle de acesso) que esse cmdlet aplica ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="a46af-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="a46af-117">-DirectServerReturn</span></span>
<span data-ttu-id="a46af-118">Especifica se esse cmdlet habilita o retorno direto do servidor.</span><span class="sxs-lookup"><span data-stu-id="a46af-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="a46af-119">Especifique $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="a46af-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="a46af-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a46af-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a46af-121">Especifica o período de tempo limite de ociosidade de TCP, em minutos, para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="a46af-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a46af-122">-InformationAction</span></span>
<span data-ttu-id="a46af-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a46af-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a46af-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a46af-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a46af-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a46af-125">Continue</span></span>
- <span data-ttu-id="a46af-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a46af-126">Ignore</span></span>
- <span data-ttu-id="a46af-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="a46af-127">Inquire</span></span>
- <span data-ttu-id="a46af-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a46af-128">SilentlyContinue</span></span>
- <span data-ttu-id="a46af-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a46af-129">Stop</span></span>
- <span data-ttu-id="a46af-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a46af-130">Suspend</span></span>

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

### <span data-ttu-id="a46af-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a46af-131">-InformationVariable</span></span>
<span data-ttu-id="a46af-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a46af-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a46af-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a46af-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="a46af-134">Especifica o nome do balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="a46af-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="a46af-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="a46af-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="a46af-136">Especifica o algoritmo de distribuição do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a46af-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="a46af-137">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a46af-137">Valid values are:</span></span> 

- <span data-ttu-id="a46af-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="a46af-138">sourceIP.</span></span>
<span data-ttu-id="a46af-139">Uma afinidade de duas tuplas: IP de origem, IP de destino</span><span class="sxs-lookup"><span data-stu-id="a46af-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="a46af-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="a46af-140">sourceIPProtocol.</span></span>
<span data-ttu-id="a46af-141">Uma afinidade de três tupla: IP de origem, IP de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="a46af-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="a46af-142">nenhuma.</span><span class="sxs-lookup"><span data-stu-id="a46af-142">none.</span></span>
<span data-ttu-id="a46af-143">Uma afinidade de cinco tuplas: IP de origem, porta de origem, IP de destino, porta de destino, protocolo</span><span class="sxs-lookup"><span data-stu-id="a46af-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="a46af-144">O valor padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="a46af-144">The default value is none.</span></span>

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

### <span data-ttu-id="a46af-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a46af-145">-LocalPort</span></span>
<span data-ttu-id="a46af-146">Especifica a porta local, privada, que este ponto de extremidade usa.</span><span class="sxs-lookup"><span data-stu-id="a46af-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="a46af-147">Os aplicativos na máquina virtual escutam nesta porta solicitações de entrada de serviço para este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46af-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="a46af-148">-Name</span></span>
<span data-ttu-id="a46af-149">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a46af-150">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a46af-150">-Profile</span></span>
<span data-ttu-id="a46af-151">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a46af-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a46af-152">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a46af-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a46af-153">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a46af-153">-Protocol</span></span>
<span data-ttu-id="a46af-154">Especifica o protocolo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="a46af-155">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a46af-155">Valid values are:</span></span> 

- <span data-ttu-id="a46af-156">Protocol</span><span class="sxs-lookup"><span data-stu-id="a46af-156">tcp</span></span> 
- <span data-ttu-id="a46af-157">grama</span><span class="sxs-lookup"><span data-stu-id="a46af-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46af-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="a46af-158">-PublicPort</span></span>
<span data-ttu-id="a46af-159">Especifica a porta pública usada pelo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="a46af-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="a46af-160">-VirtualIPName</span></span>
<span data-ttu-id="a46af-161">Especifica o nome de um endereço IP virtual que o Azure associa ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="a46af-162">Seu serviço pode ter vários IPs virtuais.</span><span class="sxs-lookup"><span data-stu-id="a46af-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="a46af-163">Para criar IPs virtuais, use o cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="a46af-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="a46af-164">-VM</span><span class="sxs-lookup"><span data-stu-id="a46af-164">-VM</span></span>
<span data-ttu-id="a46af-165">Especifica a máquina virtual à qual pertence o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a46af-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a46af-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46af-166">CommonParameters</span></span>
<span data-ttu-id="a46af-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46af-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46af-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46af-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46af-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a46af-169">INPUTS</span></span>

## <span data-ttu-id="a46af-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a46af-170">OUTPUTS</span></span>

### <span data-ttu-id="a46af-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="a46af-171">System.Object</span></span>

## <span data-ttu-id="a46af-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a46af-172">NOTES</span></span>

## <span data-ttu-id="a46af-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a46af-173">RELATED LINKS</span></span>

[<span data-ttu-id="a46af-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a46af-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="a46af-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a46af-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="a46af-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a46af-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="a46af-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a46af-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a46af-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a46af-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="a46af-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a46af-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


