---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282029"
---
# <span data-ttu-id="32ca1-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="32ca1-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="32ca1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="32ca1-103">Crie um objeto v2 de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="32ca1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32ca1-104">SYNTAX</span></span>

### <span data-ttu-id="32ca1-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32ca1-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ca1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="32ca1-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ca1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="32ca1-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ca1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32ca1-108">DESCRIPTION</span></span>
<span data-ttu-id="32ca1-109">O cmdlet New-AzNetworkWatcherConnectionMonitorObject cria um objeto v2 de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="32ca1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32ca1-110">EXAMPLES</span></span>

### <span data-ttu-id="32ca1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32ca1-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="32ca1-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="32ca1-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="32ca1-113">OS</span><span class="sxs-lookup"><span data-stu-id="32ca1-113">PARAMETERS</span></span>

### <span data-ttu-id="32ca1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ca1-114">-DefaultProfile</span></span>
<span data-ttu-id="32ca1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32ca1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32ca1-116">-Local</span><span class="sxs-lookup"><span data-stu-id="32ca1-116">-Location</span></span>
<span data-ttu-id="32ca1-117">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="32ca1-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="32ca1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="32ca1-118">-Name</span></span>
<span data-ttu-id="32ca1-119">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-119">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ca1-120">-NetworkWatcher</span></span>
<span data-ttu-id="32ca1-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="32ca1-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32ca1-122">-NetworkWatcherName</span></span>
<span data-ttu-id="32ca1-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="32ca1-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="32ca1-124">-Nota</span><span class="sxs-lookup"><span data-stu-id="32ca1-124">-Note</span></span>
<span data-ttu-id="32ca1-125">Notas associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="32ca1-126">-Saída</span><span class="sxs-lookup"><span data-stu-id="32ca1-126">-Output</span></span>
<span data-ttu-id="32ca1-127">Descreve um destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32ca1-128">-ResourceGroupName</span></span>
<span data-ttu-id="32ca1-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="32ca1-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32ca1-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="32ca1-130">-Tag</span></span>
<span data-ttu-id="32ca1-131">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="32ca1-131">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-132">-The Test</span><span class="sxs-lookup"><span data-stu-id="32ca1-132">-TestGroup</span></span>
<span data-ttu-id="32ca1-133">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="32ca1-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32ca1-134">-Confirm</span></span>
<span data-ttu-id="32ca1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32ca1-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ca1-136">-WhatIf</span></span>
<span data-ttu-id="32ca1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32ca1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ca1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32ca1-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ca1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ca1-139">CommonParameters</span></span>
<span data-ttu-id="32ca1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ca1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ca1-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32ca1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ca1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32ca1-142">INPUTS</span></span>

### <span data-ttu-id="32ca1-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="32ca1-143">None</span></span>

## <span data-ttu-id="32ca1-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32ca1-144">OUTPUTS</span></span>

### <span data-ttu-id="32ca1-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="32ca1-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="32ca1-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32ca1-146">NOTES</span></span>

## <span data-ttu-id="32ca1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32ca1-147">RELATED LINKS</span></span>
