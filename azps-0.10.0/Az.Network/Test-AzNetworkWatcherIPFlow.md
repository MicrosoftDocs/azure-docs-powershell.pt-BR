---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776477"
---
# <span data-ttu-id="76b80-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="76b80-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="76b80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76b80-102">SYNOPSIS</span></span>
<span data-ttu-id="76b80-103">Retorna se o pacote é permitido ou negado para ou de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="76b80-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="76b80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76b80-104">SYNTAX</span></span>

### <span data-ttu-id="76b80-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="76b80-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76b80-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="76b80-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76b80-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76b80-107">DESCRIPTION</span></span>
<span data-ttu-id="76b80-108">O cmdlet Test-AzNetworkWatcherIPFlow, para um recurso VM especificado e um pacote com a direção especificada usando endereços IP e portas locais e remotos, retorna se o pacote é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="76b80-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="76b80-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76b80-109">EXAMPLES</span></span>

### <span data-ttu-id="76b80-110">---Exemplo 1: executar Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="76b80-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="76b80-111">Obtenha o Inspetor de rede na central oeste dos EUA para esta assinatura e, em seguida, obtenha a VM e as interfaces de rede associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="76b80-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="76b80-112">Em seguida, para a primeira interface de rede, executa Test-AzNetworkWatcherIPFlow usando o primeiro IP da primeira interface de rede para uma conexão de saída com um IP na Internet.</span><span class="sxs-lookup"><span data-stu-id="76b80-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="76b80-113">OS</span><span class="sxs-lookup"><span data-stu-id="76b80-113">PARAMETERS</span></span>

### <span data-ttu-id="76b80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76b80-114">-AsJob</span></span>
<span data-ttu-id="76b80-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76b80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76b80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b80-116">-DefaultProfile</span></span>
<span data-ttu-id="76b80-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76b80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76b80-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="76b80-118">-Direction</span></span>
<span data-ttu-id="76b80-119">Direita.</span><span class="sxs-lookup"><span data-stu-id="76b80-119">Direction.</span></span>

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

### <span data-ttu-id="76b80-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="76b80-120">-LocalIPAddress</span></span>
<span data-ttu-id="76b80-121">Endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="76b80-121">Local IP Address.</span></span>

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

### <span data-ttu-id="76b80-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="76b80-122">-LocalPort</span></span>
<span data-ttu-id="76b80-123">Porta local.</span><span class="sxs-lookup"><span data-stu-id="76b80-123">Local Port.</span></span>

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

### <span data-ttu-id="76b80-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76b80-124">-NetworkWatcher</span></span>
<span data-ttu-id="76b80-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="76b80-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="76b80-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="76b80-126">-NetworkWatcherName</span></span>
<span data-ttu-id="76b80-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="76b80-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="76b80-128">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="76b80-128">-Protocol</span></span>
<span data-ttu-id="76b80-129">NNTP.</span><span class="sxs-lookup"><span data-stu-id="76b80-129">Protocol.</span></span>

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

### <span data-ttu-id="76b80-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="76b80-130">-RemoteIPAddress</span></span>
<span data-ttu-id="76b80-131">Endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="76b80-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="76b80-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="76b80-132">-RemotePort</span></span>
<span data-ttu-id="76b80-133">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="76b80-133">Remote port.</span></span>

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

### <span data-ttu-id="76b80-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b80-134">-ResourceGroupName</span></span>
<span data-ttu-id="76b80-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="76b80-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="76b80-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="76b80-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="76b80-137">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="76b80-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="76b80-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="76b80-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="76b80-139">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="76b80-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="76b80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b80-140">CommonParameters</span></span>
<span data-ttu-id="76b80-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b80-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b80-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b80-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76b80-143">INPUTS</span></span>

### <span data-ttu-id="76b80-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76b80-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="76b80-145">System. String</span><span class="sxs-lookup"><span data-stu-id="76b80-145">System.String</span></span>

## <span data-ttu-id="76b80-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76b80-146">OUTPUTS</span></span>

### <span data-ttu-id="76b80-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="76b80-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="76b80-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76b80-148">NOTES</span></span>
<span data-ttu-id="76b80-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="76b80-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="76b80-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76b80-150">RELATED LINKS</span></span>

[<span data-ttu-id="76b80-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76b80-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="76b80-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76b80-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="76b80-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76b80-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="76b80-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="76b80-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="76b80-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="76b80-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="76b80-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="76b80-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="76b80-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="76b80-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="76b80-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76b80-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76b80-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="76b80-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="76b80-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76b80-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76b80-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76b80-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76b80-162">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76b80-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
