---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441003"
---
# <span data-ttu-id="3ccb3-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3ccb3-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="3ccb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ccb3-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccb3-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ccb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ccb3-104">SYNTAX</span></span>

### <span data-ttu-id="3ccb3-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ccb3-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccb3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3ccb3-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ccb3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ccb3-107">DESCRIPTION</span></span>
<span data-ttu-id="3ccb3-108">O cmdlet Get-AzureRmNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="3ccb3-109">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="3ccb3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ccb3-110">EXAMPLES</span></span>

### <span data-ttu-id="3ccb3-111">--Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet--</span><span class="sxs-lookup"><span data-stu-id="3ccb3-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="3ccb3-112">Obter o próximo salto para a comunicação de saída da interface de rede principal no Vachine virtual especificado para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="3ccb3-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="3ccb3-113">OS</span><span class="sxs-lookup"><span data-stu-id="3ccb3-113">PARAMETERS</span></span>

### <span data-ttu-id="3ccb3-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="3ccb3-114">-DestinationIPAddress</span></span>
<span data-ttu-id="3ccb3-115">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-115">Destination IP address.</span></span>

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

### <span data-ttu-id="3ccb3-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ccb3-116">-NetworkWatcher</span></span>
<span data-ttu-id="3ccb3-117">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="3ccb3-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3ccb3-118">-NetworkWatcherName</span></span>
<span data-ttu-id="3ccb3-119">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="3ccb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="3ccb3-121">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3ccb3-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="3ccb3-122">-SourceIPAddress</span></span>
<span data-ttu-id="3ccb3-123">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-123">Source IP address.</span></span>

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

### <span data-ttu-id="3ccb3-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="3ccb3-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="3ccb3-125">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="3ccb3-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3ccb3-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3ccb3-127">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3ccb3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccb3-128">-DefaultProfile</span></span>
<span data-ttu-id="3ccb3-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ccb3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccb3-130">CommonParameters</span></span>
<span data-ttu-id="3ccb3-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccb3-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccb3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccb3-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ccb3-133">INPUTS</span></span>

### <span data-ttu-id="3ccb3-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ccb3-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3ccb3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3ccb3-135">System.String</span></span>

## <span data-ttu-id="3ccb3-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ccb3-136">OUTPUTS</span></span>

### <span data-ttu-id="3ccb3-137">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="3ccb3-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="3ccb3-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ccb3-138">NOTES</span></span>
<span data-ttu-id="3ccb3-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="3ccb3-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="3ccb3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ccb3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3ccb3-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ccb3-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3ccb3-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ccb3-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3ccb3-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ccb3-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3ccb3-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3ccb3-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3ccb3-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3ccb3-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3ccb3-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3ccb3-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3ccb3-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3ccb3-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3ccb3-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ccb3-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ccb3-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3ccb3-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3ccb3-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ccb3-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ccb3-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ccb3-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ccb3-152">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ccb3-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

