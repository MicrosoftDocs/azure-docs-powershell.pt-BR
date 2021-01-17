---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433389"
---
# <span data-ttu-id="fa052-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa052-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="fa052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa052-102">SYNOPSIS</span></span>
<span data-ttu-id="fa052-103">Atualiza o recurso monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="fa052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa052-104">SYNTAX</span></span>

### <span data-ttu-id="fa052-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa052-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa052-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fa052-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa052-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="fa052-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="fa052-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fa052-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="fa052-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa052-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="fa052-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa052-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa052-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa052-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa052-114">DESCRIPTION</span></span>
<span data-ttu-id="fa052-115">O cmdlet Set-AzNetworkWatcherConnectionMonitor atualiza o recurso monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="fa052-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa052-116">EXAMPLES</span></span>

### <span data-ttu-id="fa052-117">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="fa052-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="fa052-118">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="fa052-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="fa052-119">OS</span><span class="sxs-lookup"><span data-stu-id="fa052-119">PARAMETERS</span></span>

### <span data-ttu-id="fa052-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa052-120">-AsJob</span></span>
<span data-ttu-id="fa052-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fa052-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa052-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="fa052-122">-ConfigureOnly</span></span>
<span data-ttu-id="fa052-123">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="fa052-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="fa052-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa052-124">-DefaultProfile</span></span>
<span data-ttu-id="fa052-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa052-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa052-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="fa052-126">-DestinationAddress</span></span>
<span data-ttu-id="fa052-127">Endereço do destino do monitor de conexão (IP ou nome do domínio).</span><span class="sxs-lookup"><span data-stu-id="fa052-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="fa052-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="fa052-128">-DestinationPort</span></span>
<span data-ttu-id="fa052-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="fa052-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="fa052-130">-DestinationResourceId</span></span>
<span data-ttu-id="fa052-131">A ID do recurso usado como o destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="fa052-132">-Force</span><span class="sxs-lookup"><span data-stu-id="fa052-132">-Force</span></span>
<span data-ttu-id="fa052-133">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="fa052-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fa052-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa052-134">-InputObject</span></span>
<span data-ttu-id="fa052-135">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="fa052-136">-Local</span><span class="sxs-lookup"><span data-stu-id="fa052-136">-Location</span></span>
<span data-ttu-id="fa052-137">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fa052-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fa052-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fa052-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="fa052-139">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="fa052-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="fa052-140">O valor padrão é 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="fa052-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="fa052-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa052-141">-Name</span></span>
<span data-ttu-id="fa052-142">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="fa052-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa052-143">-NetworkWatcher</span></span>
<span data-ttu-id="fa052-144">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fa052-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="fa052-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fa052-145">-NetworkWatcherName</span></span>
<span data-ttu-id="fa052-146">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fa052-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="fa052-147">-Nota</span><span class="sxs-lookup"><span data-stu-id="fa052-147">-Note</span></span>
<span data-ttu-id="fa052-148">Notas associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="fa052-149">-Saída</span><span class="sxs-lookup"><span data-stu-id="fa052-149">-Output</span></span>
<span data-ttu-id="fa052-150">Descreve um destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="fa052-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa052-151">-ResourceGroupName</span></span>
<span data-ttu-id="fa052-152">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="fa052-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fa052-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa052-153">-ResourceId</span></span>
<span data-ttu-id="fa052-154">ConnectionMonitor ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="fa052-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="fa052-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="fa052-155">-SourcePort</span></span>
<span data-ttu-id="fa052-156">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="fa052-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fa052-157">-SourceResourceId</span></span>
<span data-ttu-id="fa052-158">A ID do recurso usado como a origem pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa052-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="fa052-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="fa052-159">-Tag</span></span>
<span data-ttu-id="fa052-160">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa052-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fa052-161">-The Test</span><span class="sxs-lookup"><span data-stu-id="fa052-161">-TestGroup</span></span>
<span data-ttu-id="fa052-162">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="fa052-162">The list of test groups.</span></span>

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

### <span data-ttu-id="fa052-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa052-163">-Confirm</span></span>
<span data-ttu-id="fa052-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa052-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa052-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa052-165">-WhatIf</span></span>
<span data-ttu-id="fa052-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa052-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa052-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa052-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa052-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa052-168">CommonParameters</span></span>
<span data-ttu-id="fa052-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa052-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa052-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa052-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa052-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa052-171">INPUTS</span></span>

### <span data-ttu-id="fa052-172">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa052-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fa052-173">System. String</span><span class="sxs-lookup"><span data-stu-id="fa052-173">System.String</span></span>

### <span data-ttu-id="fa052-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="fa052-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="fa052-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa052-175">OUTPUTS</span></span>

### <span data-ttu-id="fa052-176">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="fa052-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="fa052-177">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="fa052-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="fa052-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa052-178">NOTES</span></span>

## <span data-ttu-id="fa052-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa052-179">RELATED LINKS</span></span>
