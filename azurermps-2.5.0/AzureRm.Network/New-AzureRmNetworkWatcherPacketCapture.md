---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: f91dc3942241237ddf3841d276ea442361d89987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785891"
---
# <span data-ttu-id="418cc-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="418cc-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="418cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="418cc-102">SYNOPSIS</span></span>
<span data-ttu-id="418cc-103">Cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="418cc-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="418cc-104">SYNTAX</span></span>

### <span data-ttu-id="418cc-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="418cc-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418cc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="418cc-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418cc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="418cc-107">DESCRIPTION</span></span>
<span data-ttu-id="418cc-108">O cmdlet New-AzureRmNetworkWatcherPacketCapture cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="418cc-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="418cc-109">O comprimento das sessões de captura de pacotes pode ser configurado por meio de uma restrição de tempo ou de tamanho.</span><span class="sxs-lookup"><span data-stu-id="418cc-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="418cc-110">A quantidade de dados capturados para cada pacote também pode ser configurada.</span><span class="sxs-lookup"><span data-stu-id="418cc-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="418cc-111">Os filtros podem ser aplicados a uma determinada sessão de captura de pacotes, permitindo que você personalize o tipo de pacotes capturados.</span><span class="sxs-lookup"><span data-stu-id="418cc-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="418cc-112">Os filtros podem restringir pacotes em endereços IP locais e remotos & intervalos de endereços, portas locais e remotas & intervalos de porta e o protocolo em nível de sessão a ser capturado.</span><span class="sxs-lookup"><span data-stu-id="418cc-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="418cc-113">Os filtros são combináveis e vários filtros podem ser aplicados para fornecer a granularidade da captura.</span><span class="sxs-lookup"><span data-stu-id="418cc-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="418cc-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="418cc-114">EXAMPLES</span></span>

### <span data-ttu-id="418cc-115">---Exemplo 1: criar uma captura de pacotes com vários filtros---</span><span class="sxs-lookup"><span data-stu-id="418cc-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="418cc-116">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="418cc-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="418cc-117">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="418cc-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="418cc-118">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="418cc-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="418cc-119">OS</span><span class="sxs-lookup"><span data-stu-id="418cc-119">PARAMETERS</span></span>

### <span data-ttu-id="418cc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="418cc-120">-AsJob</span></span>
<span data-ttu-id="418cc-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="418cc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="418cc-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="418cc-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="418cc-123">Bytes a serem capturados por pacote.</span><span class="sxs-lookup"><span data-stu-id="418cc-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418cc-124">-DefaultProfile</span></span>
<span data-ttu-id="418cc-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="418cc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418cc-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="418cc-126">-Filter</span></span>
<span data-ttu-id="418cc-127">Filtros para sessão de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="418cc-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="418cc-128">-LocalFilePath</span></span>
<span data-ttu-id="418cc-129">Caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="418cc-129">Local file path.</span></span>

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

### <span data-ttu-id="418cc-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="418cc-130">-NetworkWatcher</span></span>
<span data-ttu-id="418cc-131">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="418cc-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="418cc-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="418cc-132">-NetworkWatcherName</span></span>
<span data-ttu-id="418cc-133">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="418cc-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="418cc-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="418cc-134">-PacketCaptureName</span></span>
<span data-ttu-id="418cc-135">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="418cc-135">The packet capture name.</span></span>

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

### <span data-ttu-id="418cc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418cc-136">-ResourceGroupName</span></span>
<span data-ttu-id="418cc-137">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="418cc-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="418cc-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="418cc-138">-StorageAccountId</span></span>
<span data-ttu-id="418cc-139">ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="418cc-139">Storage account Id.</span></span>

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

### <span data-ttu-id="418cc-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="418cc-140">-StoragePath</span></span>
<span data-ttu-id="418cc-141">Caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="418cc-141">Storage path.</span></span>

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

### <span data-ttu-id="418cc-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="418cc-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="418cc-143">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="418cc-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="418cc-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="418cc-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="418cc-145">Tempo limite em segundos.</span><span class="sxs-lookup"><span data-stu-id="418cc-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="418cc-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="418cc-147">Total de bytes por sessão.</span><span class="sxs-lookup"><span data-stu-id="418cc-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="418cc-148">-Confirm</span></span>
<span data-ttu-id="418cc-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="418cc-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418cc-150">-WhatIf</span></span>
<span data-ttu-id="418cc-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="418cc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="418cc-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="418cc-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418cc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418cc-153">CommonParameters</span></span>
<span data-ttu-id="418cc-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418cc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418cc-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418cc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418cc-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="418cc-156">INPUTS</span></span>

### <span data-ttu-id="418cc-157">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="418cc-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="418cc-158">System. String System. Anulável \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="418cc-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="418cc-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="418cc-159">OUTPUTS</span></span>

### <span data-ttu-id="418cc-160">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="418cc-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="418cc-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="418cc-161">NOTES</span></span>
<span data-ttu-id="418cc-162">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="418cc-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="418cc-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="418cc-163">RELATED LINKS</span></span>

[<span data-ttu-id="418cc-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="418cc-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="418cc-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="418cc-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="418cc-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="418cc-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="418cc-167">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="418cc-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="418cc-168">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="418cc-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="418cc-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="418cc-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="418cc-170">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="418cc-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="418cc-171">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="418cc-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="418cc-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="418cc-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="418cc-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="418cc-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="418cc-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="418cc-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="418cc-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="418cc-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


