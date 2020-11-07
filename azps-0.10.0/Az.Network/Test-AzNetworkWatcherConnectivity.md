---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: f6c25d58588d0b75f67163c50cfa91a6f8e982da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776476"
---
# <span data-ttu-id="f8bc5-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f8bc5-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="f8bc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bc5-103">Retorna informações de conectividade para uma VM de origem especificada e um destino.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="f8bc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8bc5-104">SYNTAX</span></span>

### <span data-ttu-id="f8bc5-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8bc5-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bc5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f8bc5-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8bc5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="f8bc5-108">O cmdlet Test-AzNetworkWatcherConnectivity retorna informações de conectividade para uma VM de origem especificada e um destino.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-108">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="f8bc5-109">Se não for possível estabelecer conectividade entre a origem e o destino, o cmdlet retornará detalhes sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="f8bc5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8bc5-110">EXAMPLES</span></span>

### <span data-ttu-id="f8bc5-111">---------------Exemplo 1: testar a conectividade do Inspetor de rede de uma VM para um site---------------</span><span class="sxs-lookup"><span data-stu-id="f8bc5-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="f8bc5-112">Neste exemplo, testamos a conectividade de uma VM no Azure para www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="f8bc5-113">OS</span><span class="sxs-lookup"><span data-stu-id="f8bc5-113">PARAMETERS</span></span>

### <span data-ttu-id="f8bc5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8bc5-114">-AsJob</span></span>
<span data-ttu-id="f8bc5-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f8bc5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8bc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bc5-116">-DefaultProfile</span></span>
<span data-ttu-id="f8bc5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8bc5-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f8bc5-118">-DestinationAddress</span></span>
<span data-ttu-id="f8bc5-119">O endereço IP ou URI o recurso para o qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="f8bc5-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="f8bc5-120">-DestinationId</span></span>
<span data-ttu-id="f8bc5-121">A ID do recurso para o qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="f8bc5-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f8bc5-122">-DestinationPort</span></span>
<span data-ttu-id="f8bc5-123">Porta na qual verificação de conectividade será realizada.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc5-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8bc5-124">-NetworkWatcher</span></span>
<span data-ttu-id="f8bc5-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f8bc5-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f8bc5-126">-NetworkWatcherName</span></span>
<span data-ttu-id="f8bc5-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bc5-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8bc5-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f8bc5-130">-SourceID</span><span class="sxs-lookup"><span data-stu-id="f8bc5-130">-SourceId</span></span>
<span data-ttu-id="f8bc5-131">A ID do recurso a partir do qual uma verificação de conectividade será iniciada.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="f8bc5-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f8bc5-132">-SourcePort</span></span>
<span data-ttu-id="f8bc5-133">A porta de origem da qual uma verificação de conectividade será realizada.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-133">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="f8bc5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bc5-134">CommonParameters</span></span>
<span data-ttu-id="f8bc5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bc5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8bc5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bc5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8bc5-137">INPUTS</span></span>

### <span data-ttu-id="f8bc5-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8bc5-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f8bc5-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="f8bc5-139">System.String System.Int32</span></span>

## <span data-ttu-id="f8bc5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8bc5-140">OUTPUTS</span></span>

### <span data-ttu-id="f8bc5-141">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="f8bc5-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="f8bc5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8bc5-142">NOTES</span></span>
<span data-ttu-id="f8bc5-143">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f8bc5-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="f8bc5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8bc5-144">RELATED LINKS</span></span>

<span data-ttu-id="f8bc5-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f8bc5-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="f8bc5-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f8bc5-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f8bc5-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Parar-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f8bc5-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>
