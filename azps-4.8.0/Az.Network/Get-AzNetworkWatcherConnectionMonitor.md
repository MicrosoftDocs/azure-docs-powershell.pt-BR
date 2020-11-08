---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111084"
---
# <span data-ttu-id="9f96e-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9f96e-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9f96e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f96e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f96e-103">Retorna o monitor de conexão com o nome especificado ou a lista de monitores de conexão</span><span class="sxs-lookup"><span data-stu-id="9f96e-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="9f96e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f96e-104">SYNTAX</span></span>

### <span data-ttu-id="9f96e-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f96e-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f96e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9f96e-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f96e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9f96e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f96e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f96e-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f96e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f96e-109">DESCRIPTION</span></span>
<span data-ttu-id="9f96e-110">O cmdlet Get-AzNetworkWatcherConnectionMonitor retorna o monitor de conexão com o nome/ResourceId especificado ou a lista de monitores de conexão correspondentes ao inspetor/local de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="9f96e-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="9f96e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f96e-111">EXAMPLES</span></span>

### <span data-ttu-id="9f96e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f96e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="9f96e-113">Nome: identificação cm:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: êxito fonte: {"ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/Providers/Microsoft. C ompute/virtualMachines/irinavm", "porta": 0} destino: {"endereço": "google.com", "porta": 80} MonitoringIntervalInSeconds: 60 AutoStart: true StartTime: 1/12/2018 7:19:28 PM MonitoringStatus: para o local interrompido: centraluseuap tipo: Microsoft. Network/networkWatchers/connectionMonitors Tags: {"key1": "valor1"}</span><span class="sxs-lookup"><span data-stu-id="9f96e-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="9f96e-114">OS</span><span class="sxs-lookup"><span data-stu-id="9f96e-114">PARAMETERS</span></span>

### <span data-ttu-id="9f96e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f96e-115">-DefaultProfile</span></span>
<span data-ttu-id="9f96e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f96e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f96e-117">-Local</span><span class="sxs-lookup"><span data-stu-id="9f96e-117">-Location</span></span>
<span data-ttu-id="9f96e-118">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="9f96e-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9f96e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f96e-119">-Name</span></span>
<span data-ttu-id="9f96e-120">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="9f96e-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="9f96e-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f96e-121">-NetworkWatcher</span></span>
<span data-ttu-id="9f96e-122">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="9f96e-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="9f96e-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9f96e-123">-NetworkWatcherName</span></span>
<span data-ttu-id="9f96e-124">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="9f96e-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="9f96e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f96e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f96e-126">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="9f96e-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9f96e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f96e-127">-ResourceId</span></span>
<span data-ttu-id="9f96e-128">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f96e-128">Resource ID.</span></span>

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

### <span data-ttu-id="9f96e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f96e-129">CommonParameters</span></span>
<span data-ttu-id="9f96e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f96e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f96e-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f96e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f96e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f96e-132">INPUTS</span></span>

### <span data-ttu-id="9f96e-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9f96e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9f96e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9f96e-134">System.String</span></span>

## <span data-ttu-id="9f96e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f96e-135">OUTPUTS</span></span>

### <span data-ttu-id="9f96e-136">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="9f96e-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="9f96e-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="9f96e-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="9f96e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f96e-138">NOTES</span></span>

## <span data-ttu-id="9f96e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f96e-139">RELATED LINKS</span></span>
