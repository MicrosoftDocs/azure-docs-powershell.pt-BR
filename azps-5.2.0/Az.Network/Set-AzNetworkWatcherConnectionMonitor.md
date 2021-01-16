---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260074"
---
# <span data-ttu-id="66c29-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="66c29-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="66c29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66c29-102">SYNOPSIS</span></span>
<span data-ttu-id="66c29-103">Atualiza o recurso monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="66c29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66c29-104">SYNTAX</span></span>

### <span data-ttu-id="66c29-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="66c29-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66c29-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="66c29-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66c29-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="66c29-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="66c29-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="66c29-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="66c29-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="66c29-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="66c29-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c29-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="66c29-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c29-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66c29-114">DESCRIPTION</span></span>
<span data-ttu-id="66c29-115">O cmdlet Set-AzNetworkWatcherConnectionMonitor atualiza o recurso monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="66c29-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66c29-116">EXAMPLES</span></span>

### <span data-ttu-id="66c29-117">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="66c29-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="66c29-118">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="66c29-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="66c29-119">OS</span><span class="sxs-lookup"><span data-stu-id="66c29-119">PARAMETERS</span></span>

### <span data-ttu-id="66c29-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66c29-120">-AsJob</span></span>
<span data-ttu-id="66c29-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="66c29-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66c29-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="66c29-122">-ConfigureOnly</span></span>
<span data-ttu-id="66c29-123">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="66c29-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="66c29-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c29-124">-DefaultProfile</span></span>
<span data-ttu-id="66c29-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66c29-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c29-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="66c29-126">-DestinationAddress</span></span>
<span data-ttu-id="66c29-127">Endereço do destino do monitor de conexão (IP ou nome do domínio).</span><span class="sxs-lookup"><span data-stu-id="66c29-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="66c29-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="66c29-128">-DestinationPort</span></span>
<span data-ttu-id="66c29-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="66c29-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="66c29-130">-DestinationResourceId</span></span>
<span data-ttu-id="66c29-131">A ID do recurso usado como o destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="66c29-132">-Force</span><span class="sxs-lookup"><span data-stu-id="66c29-132">-Force</span></span>
<span data-ttu-id="66c29-133">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="66c29-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="66c29-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66c29-134">-InputObject</span></span>
<span data-ttu-id="66c29-135">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="66c29-136">-Local</span><span class="sxs-lookup"><span data-stu-id="66c29-136">-Location</span></span>
<span data-ttu-id="66c29-137">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="66c29-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="66c29-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="66c29-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="66c29-139">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="66c29-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="66c29-140">O valor padrão é 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="66c29-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="66c29-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="66c29-141">-Name</span></span>
<span data-ttu-id="66c29-142">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="66c29-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66c29-143">-NetworkWatcher</span></span>
<span data-ttu-id="66c29-144">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="66c29-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="66c29-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="66c29-145">-NetworkWatcherName</span></span>
<span data-ttu-id="66c29-146">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="66c29-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="66c29-147">-Nota</span><span class="sxs-lookup"><span data-stu-id="66c29-147">-Note</span></span>
<span data-ttu-id="66c29-148">Notas associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="66c29-149">-Saída</span><span class="sxs-lookup"><span data-stu-id="66c29-149">-Output</span></span>
<span data-ttu-id="66c29-150">Descreve um destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="66c29-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c29-151">-ResourceGroupName</span></span>
<span data-ttu-id="66c29-152">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="66c29-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="66c29-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c29-153">-ResourceId</span></span>
<span data-ttu-id="66c29-154">ConnectionMonitor ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="66c29-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="66c29-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="66c29-155">-SourcePort</span></span>
<span data-ttu-id="66c29-156">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="66c29-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="66c29-157">-SourceResourceId</span></span>
<span data-ttu-id="66c29-158">A ID do recurso usado como a origem pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="66c29-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="66c29-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="66c29-159">-Tag</span></span>
<span data-ttu-id="66c29-160">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="66c29-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="66c29-161">-The Test</span><span class="sxs-lookup"><span data-stu-id="66c29-161">-TestGroup</span></span>
<span data-ttu-id="66c29-162">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="66c29-162">The list of test groups.</span></span>

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

### <span data-ttu-id="66c29-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66c29-163">-Confirm</span></span>
<span data-ttu-id="66c29-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66c29-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c29-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c29-165">-WhatIf</span></span>
<span data-ttu-id="66c29-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66c29-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c29-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66c29-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c29-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c29-168">CommonParameters</span></span>
<span data-ttu-id="66c29-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c29-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c29-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66c29-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c29-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66c29-171">INPUTS</span></span>

### <span data-ttu-id="66c29-172">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66c29-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="66c29-173">System. String</span><span class="sxs-lookup"><span data-stu-id="66c29-173">System.String</span></span>

### <span data-ttu-id="66c29-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="66c29-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="66c29-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66c29-175">OUTPUTS</span></span>

### <span data-ttu-id="66c29-176">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="66c29-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="66c29-177">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="66c29-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="66c29-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66c29-178">NOTES</span></span>

## <span data-ttu-id="66c29-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66c29-179">RELATED LINKS</span></span>
