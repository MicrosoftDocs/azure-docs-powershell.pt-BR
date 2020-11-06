---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427533"
---
# <span data-ttu-id="2022d-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2022d-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2022d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2022d-102">SYNOPSIS</span></span>
<span data-ttu-id="2022d-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="2022d-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2022d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2022d-104">SYNTAX</span></span>

### <span data-ttu-id="2022d-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2022d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2022d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2022d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2022d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2022d-107">DESCRIPTION</span></span>
<span data-ttu-id="2022d-108">O cmdlet Get-AzureRmNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="2022d-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2022d-109">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="2022d-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2022d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2022d-110">EXAMPLES</span></span>

### <span data-ttu-id="2022d-111">--Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet--</span><span class="sxs-lookup"><span data-stu-id="2022d-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="2022d-112">Obter o próximo salto para a comunicação de saída da interface de rede principal no Vachine virtual especificado para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="2022d-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2022d-113">OS</span><span class="sxs-lookup"><span data-stu-id="2022d-113">PARAMETERS</span></span>

### <span data-ttu-id="2022d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2022d-114">-AsJob</span></span>
<span data-ttu-id="2022d-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2022d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2022d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2022d-116">-DefaultProfile</span></span>
<span data-ttu-id="2022d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2022d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2022d-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2022d-118">-DestinationIPAddress</span></span>
<span data-ttu-id="2022d-119">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="2022d-119">Destination IP address.</span></span>

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

### <span data-ttu-id="2022d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2022d-120">-NetworkWatcher</span></span>
<span data-ttu-id="2022d-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2022d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2022d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2022d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2022d-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2022d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2022d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2022d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2022d-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2022d-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2022d-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2022d-126">-SourceIPAddress</span></span>
<span data-ttu-id="2022d-127">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="2022d-127">Source IP address.</span></span>

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

### <span data-ttu-id="2022d-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2022d-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2022d-129">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="2022d-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="2022d-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2022d-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2022d-131">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="2022d-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2022d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2022d-132">CommonParameters</span></span>
<span data-ttu-id="2022d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2022d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2022d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2022d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2022d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2022d-135">INPUTS</span></span>

### <span data-ttu-id="2022d-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2022d-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2022d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2022d-137">System.String</span></span>

## <span data-ttu-id="2022d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2022d-138">OUTPUTS</span></span>

### <span data-ttu-id="2022d-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2022d-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2022d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2022d-140">NOTES</span></span>
<span data-ttu-id="2022d-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="2022d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2022d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2022d-142">RELATED LINKS</span></span>

[<span data-ttu-id="2022d-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2022d-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2022d-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2022d-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2022d-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2022d-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2022d-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2022d-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2022d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2022d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2022d-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2022d-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2022d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2022d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2022d-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2022d-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2022d-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2022d-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2022d-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2022d-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2022d-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2022d-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2022d-154">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2022d-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

