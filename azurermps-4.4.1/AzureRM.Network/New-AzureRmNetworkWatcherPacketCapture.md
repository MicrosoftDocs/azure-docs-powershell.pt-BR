---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 87ae0ab7be4ace85d9f02a5637ea29dd27b0ae14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433063"
---
# <span data-ttu-id="7df59-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7df59-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7df59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7df59-102">SYNOPSIS</span></span>
<span data-ttu-id="7df59-103">Cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="7df59-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7df59-104">SYNTAX</span></span>

### <span data-ttu-id="7df59-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7df59-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df59-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7df59-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df59-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7df59-107">DESCRIPTION</span></span>
<span data-ttu-id="7df59-108">O cmdlet New-AzureRmNetworkWatcherPacketCapture cria um novo recurso de captura de pacotes e inicia uma sessão de captura de pacotes em uma VM.</span><span class="sxs-lookup"><span data-stu-id="7df59-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="7df59-109">O comprimento das sessões de captura de pacotes pode ser configurado por meio de uma restrição de tempo ou de tamanho.</span><span class="sxs-lookup"><span data-stu-id="7df59-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="7df59-110">A quantidade de dados capturados para cada pacote também pode ser configurada.</span><span class="sxs-lookup"><span data-stu-id="7df59-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="7df59-111">Os filtros podem ser aplicados a uma determinada sessão de captura de pacotes, permitindo que você personalize o tipo de pacotes capturados.</span><span class="sxs-lookup"><span data-stu-id="7df59-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="7df59-112">Os filtros podem restringir pacotes em endereços IP locais e remotos & intervalos de endereços, portas locais e remotas & intervalos de porta e o protocolo em nível de sessão a ser capturado.</span><span class="sxs-lookup"><span data-stu-id="7df59-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="7df59-113">Os filtros são combináveis e vários filtros podem ser aplicados para fornecer a granularidade da captura.</span><span class="sxs-lookup"><span data-stu-id="7df59-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="7df59-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7df59-114">EXAMPLES</span></span>

### <span data-ttu-id="7df59-115">---Exemplo 1: criar uma captura de pacotes com vários filtros---</span><span class="sxs-lookup"><span data-stu-id="7df59-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="7df59-116">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="7df59-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7df59-117">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="7df59-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="7df59-118">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="7df59-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="7df59-119">OS</span><span class="sxs-lookup"><span data-stu-id="7df59-119">PARAMETERS</span></span>

### <span data-ttu-id="7df59-120">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="7df59-120">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="7df59-121">Bytes a serem capturados por pacote.</span><span class="sxs-lookup"><span data-stu-id="7df59-121">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="7df59-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7df59-122">-Filter</span></span>
<span data-ttu-id="7df59-123">Filtros para sessão de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="7df59-123">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="7df59-124">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="7df59-124">-LocalFilePath</span></span>
<span data-ttu-id="7df59-125">Caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="7df59-125">Local file path.</span></span>

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

### <span data-ttu-id="7df59-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7df59-126">-NetworkWatcher</span></span>
<span data-ttu-id="7df59-127">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7df59-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="7df59-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7df59-128">-NetworkWatcherName</span></span>
<span data-ttu-id="7df59-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7df59-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="7df59-130">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7df59-130">-PacketCaptureName</span></span>
<span data-ttu-id="7df59-131">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="7df59-131">The packet capture name.</span></span>

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

### <span data-ttu-id="7df59-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df59-132">-ResourceGroupName</span></span>
<span data-ttu-id="7df59-133">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7df59-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7df59-134">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7df59-134">-StorageAccountId</span></span>
<span data-ttu-id="7df59-135">ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7df59-135">Storage account Id.</span></span>

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

### <span data-ttu-id="7df59-136">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="7df59-136">-StoragePath</span></span>
<span data-ttu-id="7df59-137">Caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7df59-137">Storage path.</span></span>

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

### <span data-ttu-id="7df59-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7df59-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7df59-139">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="7df59-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="7df59-140">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="7df59-140">-TimeLimitInSeconds</span></span>
<span data-ttu-id="7df59-141">Tempo limite em segundos.</span><span class="sxs-lookup"><span data-stu-id="7df59-141">Time limit in seconds.</span></span>

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

### <span data-ttu-id="7df59-142">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="7df59-142">-TotalBytesPerSession</span></span>
<span data-ttu-id="7df59-143">Total de bytes por sessão.</span><span class="sxs-lookup"><span data-stu-id="7df59-143">Total bytes per session.</span></span>

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

### <span data-ttu-id="7df59-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7df59-144">-Confirm</span></span>
<span data-ttu-id="7df59-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df59-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df59-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df59-146">-WhatIf</span></span>
<span data-ttu-id="7df59-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7df59-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df59-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7df59-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df59-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df59-149">-DefaultProfile</span></span>
<span data-ttu-id="7df59-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7df59-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df59-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df59-151">CommonParameters</span></span>
<span data-ttu-id="7df59-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df59-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df59-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df59-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df59-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7df59-154">INPUTS</span></span>

### <span data-ttu-id="7df59-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7df59-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7df59-156">System. String System. Anulável \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="7df59-156">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="7df59-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7df59-157">OUTPUTS</span></span>

### <span data-ttu-id="7df59-158">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7df59-158">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="7df59-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7df59-159">NOTES</span></span>
<span data-ttu-id="7df59-160">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="7df59-160">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="7df59-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7df59-161">RELATED LINKS</span></span>

[<span data-ttu-id="7df59-162">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7df59-162">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7df59-163">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7df59-163">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7df59-164">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7df59-164">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7df59-165">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7df59-165">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7df59-166">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7df59-166">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7df59-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7df59-167">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7df59-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7df59-168">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7df59-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7df59-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7df59-170">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7df59-170">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7df59-171">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7df59-171">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7df59-172">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7df59-172">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7df59-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7df59-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


