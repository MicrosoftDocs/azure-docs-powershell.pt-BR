---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
ms.openlocfilehash: 41c76d78ad27ff889f2dc3e7be254bcc88668023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786308"
---
# <span data-ttu-id="f8e8c-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f8e8c-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f8e8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e8c-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8e8c-104">SYNTAX</span></span>

### <span data-ttu-id="f8e8c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8e8c-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e8c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f8e8c-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e8c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e8c-108">O cmdlet Get-AzureRmNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f8e8c-109">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f8e8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="f8e8c-111">--Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet--</span><span class="sxs-lookup"><span data-stu-id="f8e8c-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="f8e8c-112">Obter o próximo salto para a comunicação de saída da interface de rede principal no Vachine virtual especificado para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="f8e8c-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f8e8c-113">OS</span><span class="sxs-lookup"><span data-stu-id="f8e8c-113">PARAMETERS</span></span>

### <span data-ttu-id="f8e8c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8e8c-114">-AsJob</span></span>
<span data-ttu-id="f8e8c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f8e8c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8e8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e8c-116">-DefaultProfile</span></span>
<span data-ttu-id="f8e8c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e8c-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="f8e8c-118">-DestinationIPAddress</span></span>
<span data-ttu-id="f8e8c-119">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-119">Destination IP address.</span></span>

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

### <span data-ttu-id="f8e8c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8e8c-120">-NetworkWatcher</span></span>
<span data-ttu-id="f8e8c-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f8e8c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f8e8c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f8e8c-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f8e8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8e8c-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f8e8c-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="f8e8c-126">-SourceIPAddress</span></span>
<span data-ttu-id="f8e8c-127">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-127">Source IP address.</span></span>

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

### <span data-ttu-id="f8e8c-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f8e8c-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f8e8c-129">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="f8e8c-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f8e8c-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f8e8c-131">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f8e8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e8c-132">CommonParameters</span></span>
<span data-ttu-id="f8e8c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e8c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e8c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e8c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8e8c-135">INPUTS</span></span>

### <span data-ttu-id="f8e8c-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8e8c-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f8e8c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e8c-137">System.String</span></span>

## <span data-ttu-id="f8e8c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8e8c-138">OUTPUTS</span></span>

### <span data-ttu-id="f8e8c-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f8e8c-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f8e8c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8e8c-140">NOTES</span></span>
<span data-ttu-id="f8e8c-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="f8e8c-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f8e8c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8e8c-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8e8c-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8e8c-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f8e8c-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8e8c-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f8e8c-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8e8c-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f8e8c-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f8e8c-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f8e8c-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f8e8c-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f8e8c-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f8e8c-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f8e8c-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f8e8c-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f8e8c-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8e8c-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8e8c-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f8e8c-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f8e8c-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8e8c-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8e8c-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8e8c-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8e8c-154">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8e8c-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

