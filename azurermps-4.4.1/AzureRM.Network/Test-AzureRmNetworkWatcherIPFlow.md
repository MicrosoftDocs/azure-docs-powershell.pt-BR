---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441035"
---
# <span data-ttu-id="c340c-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c340c-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="c340c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c340c-102">SYNOPSIS</span></span>
<span data-ttu-id="c340c-103">Retorna se o pacote é permitido ou negado para ou de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="c340c-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c340c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c340c-104">SYNTAX</span></span>

### <span data-ttu-id="c340c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="c340c-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c340c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c340c-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c340c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c340c-107">DESCRIPTION</span></span>
<span data-ttu-id="c340c-108">O cmdlet Test-AzureRmNetworkWatcherIPFlow, para um recurso VM especificado e um pacote com a direção especificada usando endereços IP e portas locais e remotos, retorna se o pacote é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="c340c-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="c340c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c340c-109">EXAMPLES</span></span>

### <span data-ttu-id="c340c-110">---Exemplo 1: executar Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="c340c-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="c340c-111">Obtenha o Inspetor de rede na central oeste dos EUA para esta assinatura e, em seguida, obtenha a VM e as interfaces de rede associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="c340c-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="c340c-112">Em seguida, para a primeira interface de rede, executa Test-AzureRmNetworkWatcherIPFlow usando o primeiro IP da primeira interface de rede para uma conexão de saída com um IP na Internet.</span><span class="sxs-lookup"><span data-stu-id="c340c-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="c340c-113">OS</span><span class="sxs-lookup"><span data-stu-id="c340c-113">PARAMETERS</span></span>

### <span data-ttu-id="c340c-114">-Direction</span><span class="sxs-lookup"><span data-stu-id="c340c-114">-Direction</span></span>
<span data-ttu-id="c340c-115">Direita.</span><span class="sxs-lookup"><span data-stu-id="c340c-115">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="c340c-116">-LocalIPAddress</span></span>
<span data-ttu-id="c340c-117">Endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="c340c-117">Local IP Address.</span></span>

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

### <span data-ttu-id="c340c-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="c340c-118">-LocalPort</span></span>
<span data-ttu-id="c340c-119">Porta local.</span><span class="sxs-lookup"><span data-stu-id="c340c-119">Local Port.</span></span>

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

### <span data-ttu-id="c340c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c340c-120">-NetworkWatcher</span></span>
<span data-ttu-id="c340c-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c340c-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c340c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="c340c-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c340c-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="c340c-124">-Protocol</span></span>
<span data-ttu-id="c340c-125">NNTP.</span><span class="sxs-lookup"><span data-stu-id="c340c-125">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="c340c-126">-RemoteIPAddress</span></span>
<span data-ttu-id="c340c-127">Endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="c340c-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="c340c-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="c340c-128">-RemotePort</span></span>
<span data-ttu-id="c340c-129">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="c340c-129">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c340c-130">-ResourceGroupName</span></span>
<span data-ttu-id="c340c-131">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c340c-131">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="c340c-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="c340c-133">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="c340c-133">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c340c-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c340c-135">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="c340c-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c340c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c340c-136">-DefaultProfile</span></span>
<span data-ttu-id="c340c-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c340c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c340c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c340c-138">CommonParameters</span></span>
<span data-ttu-id="c340c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c340c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c340c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c340c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c340c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c340c-141">INPUTS</span></span>

### <span data-ttu-id="c340c-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c340c-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c340c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c340c-143">System.String</span></span>

## <span data-ttu-id="c340c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c340c-144">OUTPUTS</span></span>

### <span data-ttu-id="c340c-145">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="c340c-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="c340c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c340c-146">NOTES</span></span>
<span data-ttu-id="c340c-147">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="c340c-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="c340c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c340c-148">RELATED LINKS</span></span>

[<span data-ttu-id="c340c-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c340c-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c340c-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c340c-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c340c-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c340c-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c340c-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c340c-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c340c-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c340c-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c340c-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c340c-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c340c-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c340c-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c340c-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c340c-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c340c-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c340c-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c340c-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c340c-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c340c-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c340c-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c340c-160">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c340c-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
