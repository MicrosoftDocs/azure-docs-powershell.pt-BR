---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429255"
---
# <span data-ttu-id="e12a1-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e12a1-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="e12a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e12a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e12a1-103">Cria um novo objeto de filtro de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="e12a1-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e12a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e12a1-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e12a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e12a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e12a1-106">O cmdlet New-AzureRmPacketCaptureFilterConfig cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="e12a1-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="e12a1-107">Esse objeto é usado para restringir o tipo de pacotes que são capturados durante uma sessão de captura de pacote usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="e12a1-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="e12a1-108">O cmdlet New-AzureRmNetworkWatcherPacketCapture pode aceitar vários objetos de filtro para habilitar as sessões de captura combináveis.</span><span class="sxs-lookup"><span data-stu-id="e12a1-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="e12a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e12a1-109">EXAMPLES</span></span>

### <span data-ttu-id="e12a1-110">---Exemplo 1: criar uma captura de pacotes com vários filtros---</span><span class="sxs-lookup"><span data-stu-id="e12a1-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="e12a1-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="e12a1-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="e12a1-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="e12a1-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="e12a1-113">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="e12a1-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="e12a1-114">OS</span><span class="sxs-lookup"><span data-stu-id="e12a1-114">PARAMETERS</span></span>

### <span data-ttu-id="e12a1-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="e12a1-115">-LocalIPAddress</span></span>
<span data-ttu-id="e12a1-116">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e12a1-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="e12a1-117">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="e12a1-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="e12a1-118">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="e12a1-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="e12a1-119">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="e12a1-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="e12a1-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="e12a1-120">-LocalPort</span></span>
<span data-ttu-id="e12a1-121">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e12a1-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="e12a1-122">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="e12a1-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="e12a1-123">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="e12a1-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="e12a1-124">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="e12a1-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="e12a1-125">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e12a1-125">-Protocol</span></span>
<span data-ttu-id="e12a1-126">Especifica o Procotol para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e12a1-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="e12a1-127">Valores aceitáveis "TCP", "UDP", "qualquer"</span><span class="sxs-lookup"><span data-stu-id="e12a1-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e12a1-128">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="e12a1-128">-RemoteIPAddress</span></span>
<span data-ttu-id="e12a1-129">Especifica o endereço IP remoto para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e12a1-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="e12a1-130">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="e12a1-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="e12a1-131">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="e12a1-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="e12a1-132">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="e12a1-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="e12a1-133">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="e12a1-133">-RemotePort</span></span>
<span data-ttu-id="e12a1-134">Especifica a porta remota para filtrar.</span><span class="sxs-lookup"><span data-stu-id="e12a1-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="e12a1-135">Entradas de exemplo de porta remota: "80" para entrada de porta única.</span><span class="sxs-lookup"><span data-stu-id="e12a1-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="e12a1-136">"80-85" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="e12a1-136">"80-85" for range.</span></span>
<span data-ttu-id="e12a1-137">"80; 443;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="e12a1-137">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="e12a1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12a1-138">-DefaultProfile</span></span>
<span data-ttu-id="e12a1-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e12a1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e12a1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12a1-140">CommonParameters</span></span>
<span data-ttu-id="e12a1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12a1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12a1-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e12a1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12a1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e12a1-143">INPUTS</span></span>

### <span data-ttu-id="e12a1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e12a1-144">System.String</span></span>

## <span data-ttu-id="e12a1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e12a1-145">OUTPUTS</span></span>

### <span data-ttu-id="e12a1-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="e12a1-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="e12a1-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e12a1-147">NOTES</span></span>
<span data-ttu-id="e12a1-148">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro</span><span class="sxs-lookup"><span data-stu-id="e12a1-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="e12a1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e12a1-149">RELATED LINKS</span></span>

[<span data-ttu-id="e12a1-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e12a1-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e12a1-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e12a1-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e12a1-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e12a1-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e12a1-153">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e12a1-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e12a1-154">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e12a1-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e12a1-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e12a1-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e12a1-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e12a1-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e12a1-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e12a1-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e12a1-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e12a1-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e12a1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e12a1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e12a1-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e12a1-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e12a1-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e12a1-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
