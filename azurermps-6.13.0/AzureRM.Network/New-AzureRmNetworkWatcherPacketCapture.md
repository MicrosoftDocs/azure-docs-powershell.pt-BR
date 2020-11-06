---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441246"
---
# <span data-ttu-id="721cf-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="721cf-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="721cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="721cf-102">SYNOPSIS</span></span>
<span data-ttu-id="721cf-103">Cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="721cf-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="721cf-104">SYNTAX</span></span>

### <span data-ttu-id="721cf-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="721cf-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="721cf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="721cf-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="721cf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="721cf-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721cf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="721cf-108">DESCRIPTION</span></span>
<span data-ttu-id="721cf-109">O cmdlet New-AzureRmNetworkWatcherPacketCapture cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="721cf-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="721cf-110">O comprimento das sessões de captura de pacotes pode ser configurado por meio de uma restrição de tempo ou de tamanho.</span><span class="sxs-lookup"><span data-stu-id="721cf-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="721cf-111">A quantidade de dados capturados para cada pacote também pode ser configurada.</span><span class="sxs-lookup"><span data-stu-id="721cf-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="721cf-112">Os filtros podem ser aplicados a uma determinada sessão de captura de pacotes, permitindo que você personalize o tipo de pacotes capturados.</span><span class="sxs-lookup"><span data-stu-id="721cf-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="721cf-113">Os filtros podem restringir pacotes em endereços IP locais e remotos & intervalos de endereços, portas locais e remotas & intervalos de porta e o protocolo em nível de sessão a ser capturado.</span><span class="sxs-lookup"><span data-stu-id="721cf-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="721cf-114">Os filtros são combináveis e vários filtros podem ser aplicados para fornecer a granularidade da captura.</span><span class="sxs-lookup"><span data-stu-id="721cf-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="721cf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="721cf-115">EXAMPLES</span></span>

### <span data-ttu-id="721cf-116">Exemplo 1: criar uma captura de pacotes com vários filtros</span><span class="sxs-lookup"><span data-stu-id="721cf-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="721cf-117">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="721cf-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="721cf-118">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="721cf-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="721cf-119">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="721cf-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="721cf-120">OS</span><span class="sxs-lookup"><span data-stu-id="721cf-120">PARAMETERS</span></span>

### <span data-ttu-id="721cf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="721cf-121">-AsJob</span></span>
<span data-ttu-id="721cf-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="721cf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="721cf-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="721cf-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="721cf-124">Bytes a serem capturados por pacote.</span><span class="sxs-lookup"><span data-stu-id="721cf-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="721cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721cf-125">-DefaultProfile</span></span>
<span data-ttu-id="721cf-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="721cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721cf-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="721cf-127">-Filter</span></span>
<span data-ttu-id="721cf-128">Filtros para sessão de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="721cf-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="721cf-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="721cf-129">-LocalFilePath</span></span>
<span data-ttu-id="721cf-130">Caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="721cf-130">Local file path.</span></span>

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

### <span data-ttu-id="721cf-131">-Local</span><span class="sxs-lookup"><span data-stu-id="721cf-131">-Location</span></span>
<span data-ttu-id="721cf-132">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="721cf-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="721cf-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="721cf-133">-NetworkWatcher</span></span>
<span data-ttu-id="721cf-134">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="721cf-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="721cf-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="721cf-135">-NetworkWatcherName</span></span>
<span data-ttu-id="721cf-136">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="721cf-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="721cf-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="721cf-137">-PacketCaptureName</span></span>
<span data-ttu-id="721cf-138">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="721cf-138">The packet capture name.</span></span>

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

### <span data-ttu-id="721cf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721cf-139">-ResourceGroupName</span></span>
<span data-ttu-id="721cf-140">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="721cf-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="721cf-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="721cf-141">-StorageAccountId</span></span>
<span data-ttu-id="721cf-142">ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="721cf-142">Storage account Id.</span></span>

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

### <span data-ttu-id="721cf-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="721cf-143">-StoragePath</span></span>
<span data-ttu-id="721cf-144">Caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="721cf-144">Storage path.</span></span>

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

### <span data-ttu-id="721cf-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="721cf-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="721cf-146">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="721cf-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="721cf-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="721cf-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="721cf-148">Tempo limite em segundos.</span><span class="sxs-lookup"><span data-stu-id="721cf-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="721cf-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="721cf-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="721cf-150">Total de bytes por sessão.</span><span class="sxs-lookup"><span data-stu-id="721cf-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="721cf-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="721cf-151">-Confirm</span></span>
<span data-ttu-id="721cf-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721cf-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721cf-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721cf-153">-WhatIf</span></span>
<span data-ttu-id="721cf-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="721cf-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721cf-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="721cf-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721cf-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721cf-156">CommonParameters</span></span>
<span data-ttu-id="721cf-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721cf-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721cf-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721cf-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721cf-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="721cf-159">INPUTS</span></span>

### <span data-ttu-id="721cf-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="721cf-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="721cf-161">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="721cf-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="721cf-162">System. String</span><span class="sxs-lookup"><span data-stu-id="721cf-162">System.String</span></span>
<span data-ttu-id="721cf-163">Parâmetros: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="721cf-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="721cf-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="721cf-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="721cf-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="721cf-165">OUTPUTS</span></span>

### <span data-ttu-id="721cf-166">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="721cf-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="721cf-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="721cf-167">NOTES</span></span>
<span data-ttu-id="721cf-168">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="721cf-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="721cf-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="721cf-169">RELATED LINKS</span></span>

[<span data-ttu-id="721cf-170">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="721cf-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="721cf-171">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="721cf-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="721cf-172">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="721cf-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="721cf-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="721cf-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="721cf-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="721cf-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="721cf-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="721cf-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="721cf-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="721cf-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="721cf-177">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="721cf-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="721cf-178">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="721cf-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="721cf-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="721cf-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="721cf-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="721cf-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="721cf-181">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="721cf-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="721cf-182">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="721cf-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="721cf-183">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="721cf-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="721cf-184">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="721cf-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="721cf-185">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="721cf-186">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="721cf-187">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="721cf-188">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="721cf-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="721cf-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="721cf-190">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="721cf-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="721cf-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="721cf-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="721cf-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="721cf-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="721cf-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="721cf-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="721cf-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="721cf-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="721cf-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="721cf-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="721cf-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


