---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 577f883affc772c01343a57a533c5ae06eccf31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610357"
---
# <span data-ttu-id="19580-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="19580-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="19580-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19580-102">SYNOPSIS</span></span>
<span data-ttu-id="19580-103">Retorna se o pacote é permitido ou negado para ou de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="19580-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19580-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19580-104">SYNTAX</span></span>

### <span data-ttu-id="19580-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="19580-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19580-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="19580-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19580-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19580-107">DESCRIPTION</span></span>
<span data-ttu-id="19580-108">O cmdlet Test-AzureRmNetworkWatcherIPFlow, para um recurso VM especificado e um pacote com a direção especificada usando endereços IP e portas locais e remotos, retorna se o pacote é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="19580-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="19580-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19580-109">EXAMPLES</span></span>

### <span data-ttu-id="19580-110">---Exemplo 1: executar Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="19580-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="19580-111">Obtenha o Inspetor de rede na central oeste dos EUA para esta assinatura e, em seguida, obtenha a VM e as interfaces de rede associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="19580-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="19580-112">Em seguida, para a primeira interface de rede, executa Test-AzureRmNetworkWatcherIPFlow usando o primeiro IP da primeira interface de rede para uma conexão de saída com um IP na Internet.</span><span class="sxs-lookup"><span data-stu-id="19580-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="19580-113">OS</span><span class="sxs-lookup"><span data-stu-id="19580-113">PARAMETERS</span></span>

### <span data-ttu-id="19580-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19580-114">-AsJob</span></span>
<span data-ttu-id="19580-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="19580-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19580-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19580-116">-DefaultProfile</span></span>
<span data-ttu-id="19580-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19580-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19580-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="19580-118">-Direction</span></span>
<span data-ttu-id="19580-119">Direita.</span><span class="sxs-lookup"><span data-stu-id="19580-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19580-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="19580-120">-LocalIPAddress</span></span>
<span data-ttu-id="19580-121">Endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="19580-121">Local IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="19580-122">-LocalPort</span></span>
<span data-ttu-id="19580-123">Porta local.</span><span class="sxs-lookup"><span data-stu-id="19580-123">Local Port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19580-124">-NetworkWatcher</span></span>
<span data-ttu-id="19580-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="19580-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="19580-126">-NetworkWatcherName</span></span>
<span data-ttu-id="19580-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="19580-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-128">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="19580-128">-Protocol</span></span>
<span data-ttu-id="19580-129">NNTP.</span><span class="sxs-lookup"><span data-stu-id="19580-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19580-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="19580-130">-RemoteIPAddress</span></span>
<span data-ttu-id="19580-131">Endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="19580-131">Remote IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="19580-132">-RemotePort</span></span>
<span data-ttu-id="19580-133">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="19580-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19580-134">-ResourceGroupName</span></span>
<span data-ttu-id="19580-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="19580-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="19580-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="19580-137">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="19580-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="19580-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="19580-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="19580-139">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="19580-139">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19580-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19580-140">CommonParameters</span></span>
<span data-ttu-id="19580-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19580-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19580-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19580-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19580-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19580-143">INPUTS</span></span>

### <span data-ttu-id="19580-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19580-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="19580-145">System. String</span><span class="sxs-lookup"><span data-stu-id="19580-145">System.String</span></span>

## <span data-ttu-id="19580-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19580-146">OUTPUTS</span></span>

### <span data-ttu-id="19580-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="19580-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="19580-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19580-148">NOTES</span></span>
<span data-ttu-id="19580-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="19580-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="19580-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19580-150">RELATED LINKS</span></span>

[<span data-ttu-id="19580-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19580-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="19580-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19580-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="19580-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19580-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="19580-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="19580-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="19580-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="19580-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="19580-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="19580-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="19580-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="19580-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="19580-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19580-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19580-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="19580-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="19580-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19580-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19580-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19580-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19580-162">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19580-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
