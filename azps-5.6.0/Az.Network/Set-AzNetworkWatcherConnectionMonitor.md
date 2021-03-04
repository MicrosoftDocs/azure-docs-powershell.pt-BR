---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e5f8e8f470570993433858a0aa1c165122c614e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892614"
---
# <span data-ttu-id="209e5-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="209e5-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="209e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="209e5-102">SYNOPSIS</span></span>
<span data-ttu-id="209e5-103">Atualiza o recurso de monitoramento de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="209e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="209e5-104">SYNTAX</span></span>

### <span data-ttu-id="209e5-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="209e5-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="209e5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="209e5-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="209e5-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="209e5-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="209e5-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="209e5-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="209e5-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="209e5-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="209e5-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209e5-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="209e5-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="209e5-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="209e5-114">DESCRIPTION</span></span>
<span data-ttu-id="209e5-115">O cmdlet Set-AzNetworkWatcherConnectionMonitor atualiza o recurso de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="209e5-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="209e5-116">EXAMPLES</span></span>

### <span data-ttu-id="209e5-117">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="209e5-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="209e5-118">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="209e5-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="209e5-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="209e5-119">PARAMETERS</span></span>

### <span data-ttu-id="209e5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="209e5-120">-AsJob</span></span>
<span data-ttu-id="209e5-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="209e5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="209e5-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="209e5-122">-ConfigureOnly</span></span>
<span data-ttu-id="209e5-123">Configure o monitor de conexão, mas não o inicie</span><span class="sxs-lookup"><span data-stu-id="209e5-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209e5-124">-DefaultProfile</span></span>
<span data-ttu-id="209e5-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="209e5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="209e5-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="209e5-126">-DestinationAddress</span></span>
<span data-ttu-id="209e5-127">Endereço do destino do monitor de conexão (IP ou nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="209e5-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="209e5-128">-DestinationPort</span></span>
<span data-ttu-id="209e5-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="209e5-130">-DestinationResourceId</span></span>
<span data-ttu-id="209e5-131">A ID do recurso usado como destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="209e5-132">-Force</span></span>
<span data-ttu-id="209e5-133">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="209e5-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="209e5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="209e5-134">-InputObject</span></span>
<span data-ttu-id="209e5-135">Objeto de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-135">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-136">-Location</span><span class="sxs-lookup"><span data-stu-id="209e5-136">-Location</span></span>
<span data-ttu-id="209e5-137">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="209e5-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="209e5-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="209e5-139">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="209e5-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="209e5-140">O valor padrão é 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="209e5-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-141">-Name</span><span class="sxs-lookup"><span data-stu-id="209e5-141">-Name</span></span>
<span data-ttu-id="209e5-142">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="209e5-143">-NetworkWatcher</span></span>
<span data-ttu-id="209e5-144">O recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="209e5-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="209e5-145">-NetworkWatcherName</span></span>
<span data-ttu-id="209e5-146">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="209e5-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-147">-Observação</span><span class="sxs-lookup"><span data-stu-id="209e5-147">-Note</span></span>
<span data-ttu-id="209e5-148">Observações associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-149">-Output</span><span class="sxs-lookup"><span data-stu-id="209e5-149">-Output</span></span>
<span data-ttu-id="209e5-150">Descreve destinos de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="209e5-151">-ResourceGroupName</span></span>
<span data-ttu-id="209e5-152">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="209e5-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="209e5-153">-ResourceId</span></span>
<span data-ttu-id="209e5-154">ID do recurso ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="209e5-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="209e5-155">-SourcePort</span></span>
<span data-ttu-id="209e5-156">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="209e5-157">-SourceResourceId</span></span>
<span data-ttu-id="209e5-158">A ID do recurso usado como a origem pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="209e5-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="209e5-159">-Tag</span></span>
<span data-ttu-id="209e5-160">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="209e5-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="209e5-161">-TestGroup</span></span>
<span data-ttu-id="209e5-162">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="209e5-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="209e5-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="209e5-163">-Confirm</span></span>
<span data-ttu-id="209e5-164">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="209e5-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="209e5-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="209e5-165">-WhatIf</span></span>
<span data-ttu-id="209e5-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="209e5-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="209e5-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="209e5-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="209e5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209e5-168">CommonParameters</span></span>
<span data-ttu-id="209e5-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="209e5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209e5-170">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="209e5-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209e5-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="209e5-171">INPUTS</span></span>

### <span data-ttu-id="209e5-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="209e5-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="209e5-173">System.String</span><span class="sxs-lookup"><span data-stu-id="209e5-173">System.String</span></span>

### <span data-ttu-id="209e5-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="209e5-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="209e5-175">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="209e5-175">OUTPUTS</span></span>

### <span data-ttu-id="209e5-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="209e5-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="209e5-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="209e5-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="209e5-178">NOTES</span><span class="sxs-lookup"><span data-stu-id="209e5-178">NOTES</span></span>

## <span data-ttu-id="209e5-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="209e5-179">RELATED LINKS</span></span>
