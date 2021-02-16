---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113477"
---
# <span data-ttu-id="2d696-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2d696-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2d696-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d696-102">SYNOPSIS</span></span>
<span data-ttu-id="2d696-103">Cria um recurso de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="2d696-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d696-104">SYNTAX</span></span>

### <span data-ttu-id="2d696-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d696-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d696-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2d696-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d696-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="2d696-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d696-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="2d696-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d696-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2d696-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d696-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="2d696-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d696-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="2d696-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d696-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d696-112">DESCRIPTION</span></span>
<span data-ttu-id="2d696-113">O cmdlet New-AzNetworkWatcherConnectionMonitor cria um recurso de monitor de conexão para origem e destino especificados (monitor de conexão SingleSourcedestination) ou conjunto de grupos de teste (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="2d696-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="2d696-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d696-114">EXAMPLES</span></span>

### <span data-ttu-id="2d696-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d696-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="2d696-116">Nome : cm Id : /subscriptions/00000000-0000-0000-00000-000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: Succeeded Source : { "ResourceId": "/subscriptions/00000000-0000-0000-00000-000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft . Compute/virtualMachines/vm", "Porta": 0 } Destino: { "Endereço": "bing.com", "Porta": 80 } MonitoringIntervalInSeconds: 60 AutoStart: True StartTime : 12/1/12/2018 7:13:11 PM MonitoringStatus: Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="2d696-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="2d696-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d696-117">PARAMETERS</span></span>

### <span data-ttu-id="2d696-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d696-118">-AsJob</span></span>
<span data-ttu-id="2d696-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d696-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d696-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="2d696-120">-ConfigureOnly</span></span>
<span data-ttu-id="2d696-121">Configure o monitor de conexão, mas não inicie-o</span><span class="sxs-lookup"><span data-stu-id="2d696-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="2d696-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2d696-122">-ConnectionMonitor</span></span>
<span data-ttu-id="2d696-123">Objeto do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d696-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d696-124">-DefaultProfile</span></span>
<span data-ttu-id="2d696-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d696-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d696-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2d696-126">-DestinationAddress</span></span>
<span data-ttu-id="2d696-127">Endereço do destino do monitor de conexão (IP ou nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="2d696-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="2d696-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2d696-128">-DestinationPort</span></span>
<span data-ttu-id="2d696-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="2d696-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="2d696-130">-DestinationResourceId</span></span>
<span data-ttu-id="2d696-131">A ID do recurso usado como destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="2d696-132">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2d696-132">-Force</span></span>
<span data-ttu-id="2d696-133">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="2d696-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2d696-134">-Local</span><span class="sxs-lookup"><span data-stu-id="2d696-134">-Location</span></span>
<span data-ttu-id="2d696-135">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="2d696-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2d696-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2d696-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="2d696-137">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="2d696-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="2d696-138">O valor padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="2d696-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="2d696-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d696-139">-Name</span></span>
<span data-ttu-id="2d696-140">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="2d696-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2d696-141">-NetworkWatcher</span></span>
<span data-ttu-id="2d696-142">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="2d696-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="2d696-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2d696-143">-NetworkWatcherName</span></span>
<span data-ttu-id="2d696-144">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="2d696-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="2d696-145">-Observação</span><span class="sxs-lookup"><span data-stu-id="2d696-145">-Note</span></span>
<span data-ttu-id="2d696-146">Anotações associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="2d696-147">-Saída</span><span class="sxs-lookup"><span data-stu-id="2d696-147">-Output</span></span>
<span data-ttu-id="2d696-148">Descreve os destinos de saída de um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="2d696-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d696-149">-ResourceGroupName</span></span>
<span data-ttu-id="2d696-150">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="2d696-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2d696-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2d696-151">-SourcePort</span></span>
<span data-ttu-id="2d696-152">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="2d696-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2d696-153">-SourceResourceId</span></span>
<span data-ttu-id="2d696-154">A ID do recurso usado como fonte pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="2d696-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="2d696-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d696-155">-Tag</span></span>
<span data-ttu-id="2d696-156">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="2d696-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2d696-157">-Grupo de Teste</span><span class="sxs-lookup"><span data-stu-id="2d696-157">-TestGroup</span></span>
<span data-ttu-id="2d696-158">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="2d696-158">The list of test groups.</span></span>

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

### <span data-ttu-id="2d696-159">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2d696-159">-Confirm</span></span>
<span data-ttu-id="2d696-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d696-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d696-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d696-161">-WhatIf</span></span>
<span data-ttu-id="2d696-162">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2d696-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d696-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d696-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d696-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d696-164">CommonParameters</span></span>
<span data-ttu-id="2d696-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d696-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d696-166">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d696-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d696-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d696-167">INPUTS</span></span>

### <span data-ttu-id="2d696-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2d696-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2d696-169">System.String</span><span class="sxs-lookup"><span data-stu-id="2d696-169">System.String</span></span>

### <span data-ttu-id="2d696-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2d696-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2d696-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2d696-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2d696-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d696-172">OUTPUTS</span></span>

### <span data-ttu-id="2d696-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="2d696-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="2d696-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="2d696-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="2d696-175">Notas</span><span class="sxs-lookup"><span data-stu-id="2d696-175">NOTES</span></span>

## <span data-ttu-id="2d696-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d696-176">RELATED LINKS</span></span>
