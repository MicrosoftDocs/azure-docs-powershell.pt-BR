---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257622"
---
# <span data-ttu-id="5f0c1-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5f0c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0c1-103">Cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="5f0c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f0c1-104">SYNTAX</span></span>

### <span data-ttu-id="5f0c1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f0c1-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0c1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5f0c1-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0c1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5f0c1-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f0c1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f0c1-108">DESCRIPTION</span></span>
<span data-ttu-id="5f0c1-109">O cmdlet New-AzNetworkWatcherPacketCapture cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="5f0c1-110">O comprimento das sessões de captura de pacotes pode ser configurado por meio de uma restrição de tempo ou de tamanho.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="5f0c1-111">A quantidade de dados capturados para cada pacote também pode ser configurada.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="5f0c1-112">Os filtros podem ser aplicados a uma determinada sessão de captura de pacotes, permitindo que você personalize o tipo de pacotes capturados.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="5f0c1-113">Os filtros podem restringir pacotes em endereços IP locais e remotos & intervalos de endereços, portas locais e remotas & intervalos de porta e o protocolo em nível de sessão a ser capturado.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="5f0c1-114">Os filtros são combináveis e vários filtros podem ser aplicados para fornecer a granularidade da captura.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="5f0c1-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-115">EXAMPLES</span></span>

### <span data-ttu-id="5f0c1-116">Exemplo 1: criar uma captura de pacotes com vários filtros</span><span class="sxs-lookup"><span data-stu-id="5f0c1-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="5f0c1-117">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5f0c1-118">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="5f0c1-119">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="5f0c1-120">OS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-120">PARAMETERS</span></span>

### <span data-ttu-id="5f0c1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f0c1-121">-AsJob</span></span>
<span data-ttu-id="5f0c1-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5f0c1-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="5f0c1-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="5f0c1-124">Bytes a serem capturados por pacote.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0c1-125">-DefaultProfile</span></span>
<span data-ttu-id="5f0c1-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5f0c1-127">-Filter</span></span>
<span data-ttu-id="5f0c1-128">Filtros para sessão de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="5f0c1-129">-LocalFilePath</span></span>
<span data-ttu-id="5f0c1-130">Caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-130">Local file path.</span></span>

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

### <span data-ttu-id="5f0c1-131">-Local</span><span class="sxs-lookup"><span data-stu-id="5f0c1-131">-Location</span></span>
<span data-ttu-id="5f0c1-132">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-132">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f0c1-133">-NetworkWatcher</span></span>
<span data-ttu-id="5f0c1-134">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="5f0c1-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5f0c1-135">-NetworkWatcherName</span></span>
<span data-ttu-id="5f0c1-136">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="5f0c1-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5f0c1-137">-PacketCaptureName</span></span>
<span data-ttu-id="5f0c1-138">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-138">The packet capture name.</span></span>

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

### <span data-ttu-id="5f0c1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f0c1-139">-ResourceGroupName</span></span>
<span data-ttu-id="5f0c1-140">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5f0c1-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5f0c1-141">-StorageAccountId</span></span>
<span data-ttu-id="5f0c1-142">ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-142">Storage account Id.</span></span>

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

### <span data-ttu-id="5f0c1-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5f0c1-143">-StoragePath</span></span>
<span data-ttu-id="5f0c1-144">Caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-144">Storage path.</span></span>

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

### <span data-ttu-id="5f0c1-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5f0c1-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5f0c1-146">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5f0c1-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="5f0c1-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="5f0c1-148">Tempo limite em segundos.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="5f0c1-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="5f0c1-150">Total de bytes por sessão.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f0c1-151">-Confirm</span></span>
<span data-ttu-id="5f0c1-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f0c1-153">-WhatIf</span></span>
<span data-ttu-id="5f0c1-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f0c1-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0c1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0c1-156">CommonParameters</span></span>
<span data-ttu-id="5f0c1-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0c1-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0c1-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f0c1-159">INPUTS</span></span>

### <span data-ttu-id="5f0c1-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f0c1-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5f0c1-161">System. String</span><span class="sxs-lookup"><span data-stu-id="5f0c1-161">System.String</span></span>

### <span data-ttu-id="5f0c1-162">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5f0c1-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5f0c1-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f0c1-163">OUTPUTS</span></span>

### <span data-ttu-id="5f0c1-164">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5f0c1-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="5f0c1-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f0c1-165">NOTES</span></span>
<span data-ttu-id="5f0c1-166">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="5f0c1-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="5f0c1-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f0c1-167">RELATED LINKS</span></span>

[<span data-ttu-id="5f0c1-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f0c1-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5f0c1-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f0c1-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5f0c1-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5f0c1-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5f0c1-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5f0c1-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5f0c1-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5f0c1-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5f0c1-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5f0c1-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5f0c1-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5f0c1-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5f0c1-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5f0c1-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5f0c1-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5f0c1-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5f0c1-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5f0c1-179">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5f0c1-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5f0c1-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f0c1-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5f0c1-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5f0c1-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5f0c1-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5f0c1-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5f0c1-183">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5f0c1-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5f0c1-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5f0c1-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5f0c1-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5f0c1-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5f0c1-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5f0c1-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5f0c1-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5f0c1-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5f0c1-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5f0c1-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5f0c1-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5f0c1-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5f0c1-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5f0c1-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5f0c1-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5f0c1-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5f0c1-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


