---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775506"
---
# <span data-ttu-id="e43a7-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e43a7-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="e43a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e43a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e43a7-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="e43a7-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="e43a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e43a7-104">SYNTAX</span></span>

### <span data-ttu-id="e43a7-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="e43a7-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43a7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e43a7-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e43a7-107">DESCRIPTION</span></span>
<span data-ttu-id="e43a7-108">O cmdlet Get-AzNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="e43a7-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="e43a7-109">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="e43a7-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="e43a7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e43a7-110">EXAMPLES</span></span>

### <span data-ttu-id="e43a7-111">--Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet--</span><span class="sxs-lookup"><span data-stu-id="e43a7-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="e43a7-112">Obter o próximo salto para a comunicação de saída da interface de rede principal no Vachine virtual especificado para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="e43a7-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="e43a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="e43a7-113">PARAMETERS</span></span>

### <span data-ttu-id="e43a7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e43a7-114">-AsJob</span></span>
<span data-ttu-id="e43a7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e43a7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e43a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43a7-116">-DefaultProfile</span></span>
<span data-ttu-id="e43a7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e43a7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43a7-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="e43a7-118">-DestinationIPAddress</span></span>
<span data-ttu-id="e43a7-119">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="e43a7-119">Destination IP address.</span></span>

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

### <span data-ttu-id="e43a7-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a7-120">-NetworkWatcher</span></span>
<span data-ttu-id="e43a7-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e43a7-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="e43a7-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e43a7-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e43a7-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e43a7-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="e43a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="e43a7-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e43a7-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e43a7-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="e43a7-126">-SourceIPAddress</span></span>
<span data-ttu-id="e43a7-127">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="e43a7-127">Source IP address.</span></span>

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

### <span data-ttu-id="e43a7-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e43a7-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e43a7-129">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e43a7-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="e43a7-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e43a7-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e43a7-131">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="e43a7-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e43a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43a7-132">CommonParameters</span></span>
<span data-ttu-id="e43a7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e43a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43a7-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43a7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43a7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e43a7-135">INPUTS</span></span>

### <span data-ttu-id="e43a7-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a7-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e43a7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e43a7-137">System.String</span></span>

## <span data-ttu-id="e43a7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e43a7-138">OUTPUTS</span></span>

### <span data-ttu-id="e43a7-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="e43a7-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="e43a7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e43a7-140">NOTES</span></span>
<span data-ttu-id="e43a7-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="e43a7-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="e43a7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e43a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="e43a7-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a7-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e43a7-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a7-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e43a7-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a7-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e43a7-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e43a7-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e43a7-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e43a7-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e43a7-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e43a7-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e43a7-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e43a7-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e43a7-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a7-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a7-151">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e43a7-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e43a7-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a7-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a7-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a7-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a7-154">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a7-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

