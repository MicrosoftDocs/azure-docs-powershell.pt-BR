---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785334"
---
# <span data-ttu-id="7a185-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a185-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7a185-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a185-102">SYNOPSIS</span></span>
<span data-ttu-id="7a185-103">Obtém informações e propriedades e status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="7a185-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a185-104">SYNTAX</span></span>

### <span data-ttu-id="7a185-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a185-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a185-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7a185-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a185-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a185-107">DESCRIPTION</span></span>
<span data-ttu-id="7a185-108">O Get-AzureRmNetworkWatcherPacketCapture Obtém as propriedades e o status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="7a185-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="7a185-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a185-109">EXAMPLES</span></span>

### <span data-ttu-id="7a185-110">---Exemplo 1: criar uma captura de pacotes com vários filtros e recuperar seu status---</span><span class="sxs-lookup"><span data-stu-id="7a185-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="7a185-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="7a185-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7a185-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="7a185-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="7a185-113">Em seguida, chamamos Get-AzureRmNetworkWatcherPacketCapture para recuperar o status da sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="7a185-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="7a185-114">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="7a185-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="7a185-115">OS</span><span class="sxs-lookup"><span data-stu-id="7a185-115">PARAMETERS</span></span>

### <span data-ttu-id="7a185-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a185-116">-AsJob</span></span>
<span data-ttu-id="7a185-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a185-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a185-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a185-118">-DefaultProfile</span></span>
<span data-ttu-id="7a185-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a185-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a185-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a185-120">-NetworkWatcher</span></span>
<span data-ttu-id="7a185-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7a185-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="7a185-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7a185-122">-NetworkWatcherName</span></span>
<span data-ttu-id="7a185-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7a185-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="7a185-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7a185-124">-PacketCaptureName</span></span>
<span data-ttu-id="7a185-125">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="7a185-125">The packet capture name.</span></span>

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

### <span data-ttu-id="7a185-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a185-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a185-127">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7a185-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7a185-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a185-128">CommonParameters</span></span>
<span data-ttu-id="7a185-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a185-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a185-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a185-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a185-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a185-131">INPUTS</span></span>

### <span data-ttu-id="7a185-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a185-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7a185-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7a185-133">System.String</span></span>

## <span data-ttu-id="7a185-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a185-134">OUTPUTS</span></span>

### <span data-ttu-id="7a185-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="7a185-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="7a185-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a185-136">NOTES</span></span>
<span data-ttu-id="7a185-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="7a185-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="7a185-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a185-138">RELATED LINKS</span></span>

[<span data-ttu-id="7a185-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a185-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a185-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7a185-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7a185-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a185-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a185-142">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a185-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a185-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a185-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a185-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a185-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a185-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a185-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a185-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7a185-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7a185-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7a185-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7a185-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7a185-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7a185-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7a185-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7a185-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7a185-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

