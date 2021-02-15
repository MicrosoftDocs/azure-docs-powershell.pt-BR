---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112763"
---
# <span data-ttu-id="22b4b-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b4b-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="22b4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="22b4b-103">Atualiza o recurso de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="22b4b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22b4b-104">SYNTAX</span></span>

### <span data-ttu-id="22b4b-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="22b4b-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22b4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="22b4b-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22b4b-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="22b4b-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="22b4b-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22b4b-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="22b4b-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22b4b-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="22b4b-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b4b-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="22b4b-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b4b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="22b4b-114">DESCRIPTION</span></span>
<span data-ttu-id="22b4b-115">O Set-AzNetworkWatcherConnectionMonitor cmdlet atualiza o recurso de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="22b4b-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22b4b-116">EXAMPLES</span></span>

### <span data-ttu-id="22b4b-117">Exemplo 1: Atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="22b4b-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="22b4b-118">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="22b4b-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="22b4b-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22b4b-119">PARAMETERS</span></span>

### <span data-ttu-id="22b4b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22b4b-120">-AsJob</span></span>
<span data-ttu-id="22b4b-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="22b4b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22b4b-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="22b4b-122">-ConfigureOnly</span></span>
<span data-ttu-id="22b4b-123">Configure o monitor de conexão, mas não inicie-o</span><span class="sxs-lookup"><span data-stu-id="22b4b-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="22b4b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b4b-124">-DefaultProfile</span></span>
<span data-ttu-id="22b4b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22b4b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b4b-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="22b4b-126">-DestinationAddress</span></span>
<span data-ttu-id="22b4b-127">Endereço do destino do monitor de conexão (IP ou nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="22b4b-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="22b4b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="22b4b-128">-DestinationPort</span></span>
<span data-ttu-id="22b4b-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="22b4b-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="22b4b-130">-DestinationResourceId</span></span>
<span data-ttu-id="22b4b-131">A ID do recurso usado como destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="22b4b-132">-Forçar</span><span class="sxs-lookup"><span data-stu-id="22b4b-132">-Force</span></span>
<span data-ttu-id="22b4b-133">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="22b4b-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="22b4b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22b4b-134">-InputObject</span></span>
<span data-ttu-id="22b4b-135">Objeto do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="22b4b-136">-Local</span><span class="sxs-lookup"><span data-stu-id="22b4b-136">-Location</span></span>
<span data-ttu-id="22b4b-137">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="22b4b-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="22b4b-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="22b4b-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="22b4b-139">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="22b4b-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="22b4b-140">O valor padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="22b4b-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="22b4b-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="22b4b-141">-Name</span></span>
<span data-ttu-id="22b4b-142">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="22b4b-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b4b-143">-NetworkWatcher</span></span>
<span data-ttu-id="22b4b-144">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="22b4b-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="22b4b-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22b4b-145">-NetworkWatcherName</span></span>
<span data-ttu-id="22b4b-146">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="22b4b-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="22b4b-147">-Observação</span><span class="sxs-lookup"><span data-stu-id="22b4b-147">-Note</span></span>
<span data-ttu-id="22b4b-148">Anotações associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="22b4b-149">-Saída</span><span class="sxs-lookup"><span data-stu-id="22b4b-149">-Output</span></span>
<span data-ttu-id="22b4b-150">Descreve os destinos de saída de um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="22b4b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b4b-151">-ResourceGroupName</span></span>
<span data-ttu-id="22b4b-152">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="22b4b-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="22b4b-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22b4b-153">-ResourceId</span></span>
<span data-ttu-id="22b4b-154">ID do recurso ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="22b4b-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="22b4b-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="22b4b-155">-SourcePort</span></span>
<span data-ttu-id="22b4b-156">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="22b4b-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="22b4b-157">-SourceResourceId</span></span>
<span data-ttu-id="22b4b-158">A ID do recurso usado como fonte pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="22b4b-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="22b4b-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="22b4b-159">-Tag</span></span>
<span data-ttu-id="22b4b-160">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="22b4b-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="22b4b-161">-Grupo de Teste</span><span class="sxs-lookup"><span data-stu-id="22b4b-161">-TestGroup</span></span>
<span data-ttu-id="22b4b-162">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="22b4b-162">The list of test groups.</span></span>

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

### <span data-ttu-id="22b4b-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="22b4b-163">-Confirm</span></span>
<span data-ttu-id="22b4b-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b4b-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b4b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b4b-165">-WhatIf</span></span>
<span data-ttu-id="22b4b-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="22b4b-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b4b-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22b4b-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b4b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b4b-168">CommonParameters</span></span>
<span data-ttu-id="22b4b-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b4b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b4b-170">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22b4b-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b4b-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="22b4b-171">INPUTS</span></span>

### <span data-ttu-id="22b4b-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b4b-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="22b4b-173">System.String</span><span class="sxs-lookup"><span data-stu-id="22b4b-173">System.String</span></span>

### <span data-ttu-id="22b4b-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="22b4b-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="22b4b-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="22b4b-175">OUTPUTS</span></span>

### <span data-ttu-id="22b4b-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="22b4b-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="22b4b-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="22b4b-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="22b4b-178">Notas</span><span class="sxs-lookup"><span data-stu-id="22b4b-178">NOTES</span></span>

## <span data-ttu-id="22b4b-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22b4b-179">RELATED LINKS</span></span>
