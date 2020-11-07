---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 77a760fd78b06d4f04d5a805b689139977433f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775367"
---
# <span data-ttu-id="ac2cc-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ac2cc-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="ac2cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2cc-103">Cria um novo objeto de filtro de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="ac2cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac2cc-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac2cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac2cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ac2cc-106">O cmdlet New-AzPacketCaptureFilterConfig cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="ac2cc-107">Esse objeto é usado para restringir o tipo de pacotes que são capturados durante uma sessão de captura de pacote usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="ac2cc-108">O cmdlet New-AzNetworkWatcherPacketCapture pode aceitar vários objetos de filtro para habilitar as sessões de captura combináveis.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="ac2cc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac2cc-109">EXAMPLES</span></span>

### <span data-ttu-id="ac2cc-110">---Exemplo 1: criar uma captura de pacotes com vários filtros---</span><span class="sxs-lookup"><span data-stu-id="ac2cc-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="ac2cc-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ac2cc-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="ac2cc-113">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ac2cc-114">OS</span><span class="sxs-lookup"><span data-stu-id="ac2cc-114">PARAMETERS</span></span>

### <span data-ttu-id="ac2cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac2cc-115">-DefaultProfile</span></span>
<span data-ttu-id="ac2cc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac2cc-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="ac2cc-117">-LocalIPAddress</span></span>
<span data-ttu-id="ac2cc-118">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="ac2cc-119">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ac2cc-120">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ac2cc-121">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ac2cc-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="ac2cc-122">-LocalPort</span></span>
<span data-ttu-id="ac2cc-123">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="ac2cc-124">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ac2cc-125">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ac2cc-126">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ac2cc-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="ac2cc-127">-Protocol</span></span>
<span data-ttu-id="ac2cc-128">Especifica o Procotol para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="ac2cc-129">Valores aceitáveis "TCP", "UDP", "qualquer"</span><span class="sxs-lookup"><span data-stu-id="ac2cc-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac2cc-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="ac2cc-130">-RemoteIPAddress</span></span>
<span data-ttu-id="ac2cc-131">Especifica o endereço IP remoto para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="ac2cc-132">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ac2cc-133">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ac2cc-134">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ac2cc-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="ac2cc-135">-RemotePort</span></span>
<span data-ttu-id="ac2cc-136">Especifica a porta remota para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="ac2cc-137">Entradas de exemplo de porta remota: "80" para entrada de porta única.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="ac2cc-138">"80-85" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-138">"80-85" for range.</span></span>
<span data-ttu-id="ac2cc-139">"80; 443;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="ac2cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac2cc-140">CommonParameters</span></span>
<span data-ttu-id="ac2cc-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac2cc-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac2cc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac2cc-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac2cc-143">INPUTS</span></span>

### <span data-ttu-id="ac2cc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ac2cc-144">System.String</span></span>

## <span data-ttu-id="ac2cc-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac2cc-145">OUTPUTS</span></span>

### <span data-ttu-id="ac2cc-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="ac2cc-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="ac2cc-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac2cc-147">NOTES</span></span>
<span data-ttu-id="ac2cc-148">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro</span><span class="sxs-lookup"><span data-stu-id="ac2cc-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="ac2cc-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac2cc-149">RELATED LINKS</span></span>

[<span data-ttu-id="ac2cc-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac2cc-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac2cc-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac2cc-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac2cc-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac2cc-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac2cc-153">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac2cc-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac2cc-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac2cc-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ac2cc-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac2cc-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ac2cc-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac2cc-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ac2cc-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ac2cc-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ac2cc-158">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ac2cc-158">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ac2cc-159">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ac2cc-159">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ac2cc-160">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ac2cc-160">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ac2cc-161">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ac2cc-161">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
