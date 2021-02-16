---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: e717c32b817dc86de2bfa1b9de09b95121609f28
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416151"
---
# <span data-ttu-id="81070-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="81070-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="81070-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81070-102">SYNOPSIS</span></span>
<span data-ttu-id="81070-103">Retorna informações de conectividade para um VM de origem especificado e um destino.</span><span class="sxs-lookup"><span data-stu-id="81070-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="81070-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81070-104">SYNTAX</span></span>

### <span data-ttu-id="81070-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="81070-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81070-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="81070-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81070-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="81070-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81070-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="81070-108">DESCRIPTION</span></span>
<span data-ttu-id="81070-109">O Test-AzNetworkWatcherConnectivity cmdlet retorna informações de conectividade para um VM de origem especificado e um destino.</span><span class="sxs-lookup"><span data-stu-id="81070-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="81070-110">Se a conectividade entre a origem e o destino não puder ser estabelecida, o cmdlet retornará detalhes sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="81070-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="81070-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81070-111">EXAMPLES</span></span>

### <span data-ttu-id="81070-112">Exemplo 1: Testar a conectividade do Watcher de Rede de um VM para um site</span><span class="sxs-lookup"><span data-stu-id="81070-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
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

<span data-ttu-id="81070-113">Neste exemplo, testamos a conectividade de um VM no Azure para www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="81070-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="81070-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81070-114">Example 2</span></span>

<span data-ttu-id="81070-115">Retorna informações de conectividade para um VM de origem especificado e um destino.</span><span class="sxs-lookup"><span data-stu-id="81070-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="81070-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="81070-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="81070-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81070-117">PARAMETERS</span></span>

### <span data-ttu-id="81070-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81070-118">-AsJob</span></span>
<span data-ttu-id="81070-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="81070-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81070-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81070-120">-DefaultProfile</span></span>
<span data-ttu-id="81070-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="81070-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81070-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="81070-122">-DestinationAddress</span></span>
<span data-ttu-id="81070-123">O endereço IP ou o URI do recurso ao qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="81070-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="81070-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="81070-124">-DestinationId</span></span>
<span data-ttu-id="81070-125">A ID do recurso ao qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="81070-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="81070-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="81070-126">-DestinationPort</span></span>
<span data-ttu-id="81070-127">Porta na qual a conectividade de verificação será executada.</span><span class="sxs-lookup"><span data-stu-id="81070-127">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81070-128">-Local</span><span class="sxs-lookup"><span data-stu-id="81070-128">-Location</span></span>
<span data-ttu-id="81070-129">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="81070-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="81070-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81070-130">-NetworkWatcher</span></span>
<span data-ttu-id="81070-131">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="81070-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="81070-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="81070-132">-NetworkWatcherName</span></span>
<span data-ttu-id="81070-133">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="81070-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81070-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="81070-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="81070-135">Configuração de protocolo na qual a conectividade de verificação será executada.</span><span class="sxs-lookup"><span data-stu-id="81070-135">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81070-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81070-136">-ResourceGroupName</span></span>
<span data-ttu-id="81070-137">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="81070-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="81070-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="81070-138">-SourceId</span></span>
<span data-ttu-id="81070-139">A ID do recurso a partir do qual uma verificação de conectividade será iniciada.</span><span class="sxs-lookup"><span data-stu-id="81070-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="81070-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="81070-140">-SourcePort</span></span>
<span data-ttu-id="81070-141">A porta de origem da qual uma verificação de conectividade será executada.</span><span class="sxs-lookup"><span data-stu-id="81070-141">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81070-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81070-142">CommonParameters</span></span>
<span data-ttu-id="81070-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81070-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81070-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81070-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81070-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="81070-145">INPUTS</span></span>

### <span data-ttu-id="81070-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81070-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="81070-147">System.String</span><span class="sxs-lookup"><span data-stu-id="81070-147">System.String</span></span>

### <span data-ttu-id="81070-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="81070-148">System.Int32</span></span>

## <span data-ttu-id="81070-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="81070-149">OUTPUTS</span></span>

### <span data-ttu-id="81070-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="81070-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="81070-151">Notas</span><span class="sxs-lookup"><span data-stu-id="81070-151">NOTES</span></span>
<span data-ttu-id="81070-152">Palavras-chave: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="81070-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="81070-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81070-153">RELATED LINKS</span></span>

<span data-ttu-id="81070-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="81070-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="81070-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="81070-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="81070-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="81070-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="81070-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="81070-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
