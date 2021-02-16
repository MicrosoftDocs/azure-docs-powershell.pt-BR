---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118305"
---
# <span data-ttu-id="d6d0d-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="d6d0d-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="d6d0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d0d-103">Criar um objeto de monitor de conexão V2.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="d6d0d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6d0d-104">SYNTAX</span></span>

### <span data-ttu-id="d6d0d-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6d0d-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d0d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d6d0d-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d0d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d6d0d-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6d0d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6d0d-108">DESCRIPTION</span></span>
<span data-ttu-id="d6d0d-109">O New-AzNetworkWatcherConnectionMonitorObject cmdlet cria um objeto do monitor de conexão V2.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="d6d0d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="d6d0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6d0d-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="d6d0d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="d6d0d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="d6d0d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6d0d-113">PARAMETERS</span></span>

### <span data-ttu-id="d6d0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d0d-114">-DefaultProfile</span></span>
<span data-ttu-id="d6d0d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d0d-116">-Local</span><span class="sxs-lookup"><span data-stu-id="d6d0d-116">-Location</span></span>
<span data-ttu-id="d6d0d-117">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d6d0d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6d0d-118">-Name</span></span>
<span data-ttu-id="d6d0d-119">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-119">The connection monitor name.</span></span>

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

### <span data-ttu-id="d6d0d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6d0d-120">-NetworkWatcher</span></span>
<span data-ttu-id="d6d0d-121">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d6d0d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d6d0d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d6d0d-123">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d6d0d-124">-Observação</span><span class="sxs-lookup"><span data-stu-id="d6d0d-124">-Note</span></span>
<span data-ttu-id="d6d0d-125">Anotações associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="d6d0d-126">-Saída</span><span class="sxs-lookup"><span data-stu-id="d6d0d-126">-Output</span></span>
<span data-ttu-id="d6d0d-127">Descreve os destinos de saída de um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-127">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="d6d0d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6d0d-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6d0d-129">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d6d0d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6d0d-130">-Tag</span></span>
<span data-ttu-id="d6d0d-131">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-131">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d6d0d-132">-Grupo de Teste</span><span class="sxs-lookup"><span data-stu-id="d6d0d-132">-TestGroup</span></span>
<span data-ttu-id="d6d0d-133">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-133">The list of test groups.</span></span>

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

### <span data-ttu-id="d6d0d-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d6d0d-134">-Confirm</span></span>
<span data-ttu-id="d6d0d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d0d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d0d-136">-WhatIf</span></span>
<span data-ttu-id="d6d0d-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d0d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d0d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d0d-139">CommonParameters</span></span>
<span data-ttu-id="d6d0d-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d0d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d0d-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6d0d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d0d-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6d0d-142">INPUTS</span></span>

### <span data-ttu-id="d6d0d-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d6d0d-143">None</span></span>

## <span data-ttu-id="d6d0d-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6d0d-144">OUTPUTS</span></span>

### <span data-ttu-id="d6d0d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="d6d0d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="d6d0d-146">Notas</span><span class="sxs-lookup"><span data-stu-id="d6d0d-146">NOTES</span></span>

## <span data-ttu-id="d6d0d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6d0d-147">RELATED LINKS</span></span>
