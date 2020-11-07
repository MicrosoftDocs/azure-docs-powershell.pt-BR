---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775504"
---
# <span data-ttu-id="c05a6-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c05a6-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c05a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c05a6-102">SYNOPSIS</span></span>
<span data-ttu-id="c05a6-103">Obtém informações e propriedades e status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="c05a6-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="c05a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c05a6-104">SYNTAX</span></span>

### <span data-ttu-id="c05a6-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="c05a6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c05a6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c05a6-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05a6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c05a6-107">DESCRIPTION</span></span>
<span data-ttu-id="c05a6-108">O Get-AzNetworkWatcherPacketCapture Obtém as propriedades e o status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="c05a6-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="c05a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c05a6-109">EXAMPLES</span></span>

### <span data-ttu-id="c05a6-110">---Exemplo 1: criar uma captura de pacotes com vários filtros e recuperar seu status---</span><span class="sxs-lookup"><span data-stu-id="c05a6-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c05a6-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="c05a6-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c05a6-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="c05a6-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="c05a6-113">Em seguida, chamamos Get-AzNetworkWatcherPacketCapture para recuperar o status da sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="c05a6-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="c05a6-114">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="c05a6-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="c05a6-115">OS</span><span class="sxs-lookup"><span data-stu-id="c05a6-115">PARAMETERS</span></span>

### <span data-ttu-id="c05a6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c05a6-116">-AsJob</span></span>
<span data-ttu-id="c05a6-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c05a6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c05a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05a6-118">-DefaultProfile</span></span>
<span data-ttu-id="c05a6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c05a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c05a6-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c05a6-120">-NetworkWatcher</span></span>
<span data-ttu-id="c05a6-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c05a6-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="c05a6-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c05a6-122">-NetworkWatcherName</span></span>
<span data-ttu-id="c05a6-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c05a6-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="c05a6-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c05a6-124">-PacketCaptureName</span></span>
<span data-ttu-id="c05a6-125">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="c05a6-125">The packet capture name.</span></span>

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

### <span data-ttu-id="c05a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="c05a6-127">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c05a6-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c05a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05a6-128">CommonParameters</span></span>
<span data-ttu-id="c05a6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05a6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05a6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05a6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c05a6-131">INPUTS</span></span>

### <span data-ttu-id="c05a6-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c05a6-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c05a6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c05a6-133">System.String</span></span>

## <span data-ttu-id="c05a6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c05a6-134">OUTPUTS</span></span>

### <span data-ttu-id="c05a6-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="c05a6-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="c05a6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c05a6-136">NOTES</span></span>
<span data-ttu-id="c05a6-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="c05a6-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c05a6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c05a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="c05a6-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c05a6-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c05a6-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c05a6-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c05a6-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c05a6-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c05a6-142">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c05a6-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c05a6-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c05a6-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c05a6-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c05a6-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c05a6-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c05a6-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c05a6-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c05a6-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c05a6-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c05a6-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c05a6-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c05a6-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c05a6-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c05a6-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c05a6-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c05a6-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

