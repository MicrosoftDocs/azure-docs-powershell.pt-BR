---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609769"
---
# <span data-ttu-id="55738-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="55738-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55738-102">SYNOPSIS</span></span>
<span data-ttu-id="55738-103">Retorna o monitor de conexão com o nome especificado ou a lista de monitores de conexão</span><span class="sxs-lookup"><span data-stu-id="55738-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55738-104">SYNTAX</span></span>

### <span data-ttu-id="55738-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="55738-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55738-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="55738-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55738-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="55738-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55738-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55738-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55738-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55738-109">DESCRIPTION</span></span>
<span data-ttu-id="55738-110">O cmdlet Get-AzureRmNetworkWatcherConnectionMonitor retorna o monitor de conexão com o nome/ResourceId especificado ou a lista de monitores de conexão correspondentes ao inspetor/local de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="55738-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="55738-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55738-111">EXAMPLES</span></span>

### <span data-ttu-id="55738-112">Exemplo 1: obter o monitor de conexão por nome no local especificado</span><span class="sxs-lookup"><span data-stu-id="55738-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="55738-113">Neste exemplo, obtemos o monitor de conexão por nome no local especificado.</span><span class="sxs-lookup"><span data-stu-id="55738-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="55738-114">OS</span><span class="sxs-lookup"><span data-stu-id="55738-114">PARAMETERS</span></span>

### <span data-ttu-id="55738-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55738-115">-DefaultProfile</span></span>
<span data-ttu-id="55738-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55738-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55738-117">-Local</span><span class="sxs-lookup"><span data-stu-id="55738-117">-Location</span></span>
<span data-ttu-id="55738-118">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="55738-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="55738-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="55738-119">-Name</span></span>
<span data-ttu-id="55738-120">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="55738-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55738-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55738-121">-NetworkWatcher</span></span>
<span data-ttu-id="55738-122">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="55738-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="55738-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="55738-123">-NetworkWatcherName</span></span>
<span data-ttu-id="55738-124">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="55738-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55738-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55738-125">-ResourceGroupName</span></span>
<span data-ttu-id="55738-126">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="55738-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55738-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55738-127">-ResourceId</span></span>
<span data-ttu-id="55738-128">ID do recurso do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="55738-128">Resource ID of the connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55738-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55738-129">CommonParameters</span></span>
<span data-ttu-id="55738-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55738-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55738-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55738-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55738-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55738-132">INPUTS</span></span>

### <span data-ttu-id="55738-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55738-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="55738-134">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55738-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="55738-135">System. String</span><span class="sxs-lookup"><span data-stu-id="55738-135">System.String</span></span>

## <span data-ttu-id="55738-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55738-136">OUTPUTS</span></span>

### <span data-ttu-id="55738-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="55738-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="55738-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55738-138">NOTES</span></span>
<span data-ttu-id="55738-139">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="55738-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="55738-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55738-140">RELATED LINKS</span></span>

[<span data-ttu-id="55738-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55738-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="55738-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55738-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="55738-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55738-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="55738-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="55738-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="55738-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="55738-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="55738-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="55738-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="55738-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="55738-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="55738-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55738-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="55738-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="55738-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="55738-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55738-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="55738-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55738-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="55738-152">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55738-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="55738-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="55738-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="55738-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-157">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-158">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-159">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="55738-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="55738-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="55738-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="55738-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="55738-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="55738-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="55738-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="55738-163">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55738-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="55738-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="55738-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="55738-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="55738-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="55738-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="55738-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="55738-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="55738-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
