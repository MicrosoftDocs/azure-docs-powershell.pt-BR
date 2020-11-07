---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775509"
---
# <span data-ttu-id="fd716-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd716-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="fd716-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd716-102">SYNOPSIS</span></span>
<span data-ttu-id="fd716-103">Retorna o monitor de conexão com o nome especificado ou a lista de monitores de conexão</span><span class="sxs-lookup"><span data-stu-id="fd716-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="fd716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd716-104">SYNTAX</span></span>

### <span data-ttu-id="fd716-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd716-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fd716-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fd716-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fd716-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fd716-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fd716-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd716-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="fd716-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd716-109">DESCRIPTION</span></span>
<span data-ttu-id="fd716-110">O cmdlet Get-AzNetworkWatcherConnectionMonitor retorna o monitor de conexão com o nome/ResourceId especificado ou a lista de monitores de conexão correspondentes ao inspetor/local de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="fd716-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="fd716-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd716-111">EXAMPLES</span></span>

### <span data-ttu-id="fd716-112">---------------Exemplo 1: obter o monitor de conexão por nome no local especificado---------------</span><span class="sxs-lookup"><span data-stu-id="fd716-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="fd716-113">Neste exemplo, obtemos o monitor de conexão por nome no local especificado.</span><span class="sxs-lookup"><span data-stu-id="fd716-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="fd716-114">OS</span><span class="sxs-lookup"><span data-stu-id="fd716-114">PARAMETERS</span></span>

### <span data-ttu-id="fd716-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd716-115">-AsJob</span></span>
<span data-ttu-id="fd716-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fd716-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd716-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd716-117">-DefaultProfile</span></span>
<span data-ttu-id="fd716-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd716-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd716-119">-Local</span><span class="sxs-lookup"><span data-stu-id="fd716-119">-Location</span></span>
<span data-ttu-id="fd716-120">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fd716-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd716-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd716-121">-Name</span></span>
<span data-ttu-id="fd716-122">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fd716-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd716-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd716-123">-NetworkWatcher</span></span>
<span data-ttu-id="fd716-124">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fd716-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="fd716-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fd716-125">-NetworkWatcherName</span></span>
<span data-ttu-id="fd716-126">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fd716-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd716-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd716-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd716-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fd716-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fd716-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd716-129">-ResourceId</span></span>
<span data-ttu-id="fd716-130">ID do recurso do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fd716-130">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd716-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd716-131">CommonParameters</span></span>
<span data-ttu-id="fd716-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd716-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd716-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd716-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd716-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd716-134">INPUTS</span></span>

### <span data-ttu-id="fd716-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd716-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fd716-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd716-136">System.String</span></span>


## <span data-ttu-id="fd716-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd716-137">OUTPUTS</span></span>

### <span data-ttu-id="fd716-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="fd716-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="fd716-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd716-139">NOTES</span></span>
<span data-ttu-id="fd716-140">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="fd716-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="fd716-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd716-141">RELATED LINKS</span></span>
<span data-ttu-id="fd716-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="fd716-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="fd716-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="fd716-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="fd716-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Parar-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="fd716-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="fd716-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="fd716-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>