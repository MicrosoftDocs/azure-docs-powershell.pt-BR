---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785496"
---
# <span data-ttu-id="bc693-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc693-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bc693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc693-102">SYNOPSIS</span></span>
<span data-ttu-id="bc693-103">Retorna o monitor de conexão com o nome especificado ou a lista de monitores de conexão</span><span class="sxs-lookup"><span data-stu-id="bc693-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc693-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc693-104">SYNTAX</span></span>

### <span data-ttu-id="bc693-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc693-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bc693-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bc693-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bc693-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bc693-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bc693-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc693-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="bc693-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc693-109">DESCRIPTION</span></span>
<span data-ttu-id="bc693-110">O cmdlet Get-AzureRmNetworkWatcherConnectionMonitor retorna o monitor de conexão com o nome/ResourceId especificado ou a lista de monitores de conexão correspondentes ao inspetor/local de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="bc693-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="bc693-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc693-111">EXAMPLES</span></span>

### <span data-ttu-id="bc693-112">---------------Exemplo 1: obter o monitor de conexão por nome no local especificado---------------</span><span class="sxs-lookup"><span data-stu-id="bc693-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
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

<span data-ttu-id="bc693-113">Neste exemplo, obtemos o monitor de conexão por nome no local especificado.</span><span class="sxs-lookup"><span data-stu-id="bc693-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="bc693-114">OS</span><span class="sxs-lookup"><span data-stu-id="bc693-114">PARAMETERS</span></span>

### <span data-ttu-id="bc693-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc693-115">-AsJob</span></span>
<span data-ttu-id="bc693-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bc693-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc693-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc693-117">-DefaultProfile</span></span>
<span data-ttu-id="bc693-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc693-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc693-119">-Local</span><span class="sxs-lookup"><span data-stu-id="bc693-119">-Location</span></span>
<span data-ttu-id="bc693-120">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="bc693-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bc693-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc693-121">-Name</span></span>
<span data-ttu-id="bc693-122">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc693-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="bc693-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc693-123">-NetworkWatcher</span></span>
<span data-ttu-id="bc693-124">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="bc693-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="bc693-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bc693-125">-NetworkWatcherName</span></span>
<span data-ttu-id="bc693-126">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="bc693-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="bc693-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc693-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc693-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="bc693-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bc693-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc693-129">-ResourceId</span></span>
<span data-ttu-id="bc693-130">ID do recurso do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc693-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="bc693-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc693-131">CommonParameters</span></span>
<span data-ttu-id="bc693-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc693-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc693-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc693-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc693-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc693-134">INPUTS</span></span>

### <span data-ttu-id="bc693-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc693-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bc693-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bc693-136">System.String</span></span>


## <span data-ttu-id="bc693-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc693-137">OUTPUTS</span></span>

### <span data-ttu-id="bc693-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bc693-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="bc693-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc693-139">NOTES</span></span>
<span data-ttu-id="bc693-140">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="bc693-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="bc693-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc693-141">RELATED LINKS</span></span>
<span data-ttu-id="bc693-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="bc693-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="bc693-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="bc693-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="bc693-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="bc693-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="bc693-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="bc693-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
