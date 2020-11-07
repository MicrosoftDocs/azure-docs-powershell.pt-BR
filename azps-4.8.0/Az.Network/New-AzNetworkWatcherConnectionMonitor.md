---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954842"
---
# <span data-ttu-id="a76a7-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a76a7-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a76a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a76a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a76a7-103">Cria um recurso de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="a76a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a76a7-104">SYNTAX</span></span>

### <span data-ttu-id="a76a7-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a76a7-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a76a7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a76a7-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a76a7-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="a76a7-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76a7-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="a76a7-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76a7-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a76a7-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76a7-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="a76a7-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76a7-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="a76a7-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76a7-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a76a7-112">DESCRIPTION</span></span>
<span data-ttu-id="a76a7-113">O cmdlet New-AzNetworkWatcherConnectionMonitor cria um recurso de monitor de conexão para a origem e o destino especificados (monitor de conexão SingleSourcedestination) ou conjunto de grupos de teste (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="a76a7-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="a76a7-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a76a7-114">EXAMPLES</span></span>

### <span data-ttu-id="a76a7-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a76a7-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="a76a7-116">Nome: identificação cm:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 ETag: W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: êxito fonte: {"ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/Providers/Microsoft. Compute/virtualMachines/VM "," porta ": 0} destino: {" endereço ":" bing.com "," porta ": 80} MonitoringIntervalInSeconds: 60 AutoStart: true StartTime: 1/12/2018 7:13:11 PM MonitoringStatus: Running Location: centraluseuap Type: Microsoft. Network/networkWatchers/connectionMonitors Tags: {}</span><span class="sxs-lookup"><span data-stu-id="a76a7-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="a76a7-117">OS</span><span class="sxs-lookup"><span data-stu-id="a76a7-117">PARAMETERS</span></span>

### <span data-ttu-id="a76a7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76a7-118">-AsJob</span></span>
<span data-ttu-id="a76a7-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a76a7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76a7-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a76a7-120">-ConfigureOnly</span></span>
<span data-ttu-id="a76a7-121">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="a76a7-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a76a7-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a76a7-122">-ConnectionMonitor</span></span>
<span data-ttu-id="a76a7-123">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="a76a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76a7-124">-DefaultProfile</span></span>
<span data-ttu-id="a76a7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a76a7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a76a7-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a76a7-126">-DestinationAddress</span></span>
<span data-ttu-id="a76a7-127">Endereço do destino do monitor de conexão (IP ou nome do domínio).</span><span class="sxs-lookup"><span data-stu-id="a76a7-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="a76a7-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a76a7-128">-DestinationPort</span></span>
<span data-ttu-id="a76a7-129">A porta de destino usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="a76a7-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a76a7-130">-DestinationResourceId</span></span>
<span data-ttu-id="a76a7-131">A ID do recurso usado como o destino pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="a76a7-132">-Force</span><span class="sxs-lookup"><span data-stu-id="a76a7-132">-Force</span></span>
<span data-ttu-id="a76a7-133">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="a76a7-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a76a7-134">-Local</span><span class="sxs-lookup"><span data-stu-id="a76a7-134">-Location</span></span>
<span data-ttu-id="a76a7-135">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a76a7-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a76a7-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a76a7-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a76a7-137">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="a76a7-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="a76a7-138">O valor padrão é 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76a7-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="a76a7-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a76a7-139">-Name</span></span>
<span data-ttu-id="a76a7-140">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="a76a7-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a76a7-141">-NetworkWatcher</span></span>
<span data-ttu-id="a76a7-142">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a76a7-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="a76a7-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a76a7-143">-NetworkWatcherName</span></span>
<span data-ttu-id="a76a7-144">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a76a7-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="a76a7-145">-Nota</span><span class="sxs-lookup"><span data-stu-id="a76a7-145">-Note</span></span>
<span data-ttu-id="a76a7-146">Notas associadas ao monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="a76a7-147">-Saída</span><span class="sxs-lookup"><span data-stu-id="a76a7-147">-Output</span></span>
<span data-ttu-id="a76a7-148">Descreve um destino de saída do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="a76a7-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76a7-149">-ResourceGroupName</span></span>
<span data-ttu-id="a76a7-150">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a76a7-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a76a7-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a76a7-151">-SourcePort</span></span>
<span data-ttu-id="a76a7-152">A porta de origem usada pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="a76a7-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a76a7-153">-SourceResourceId</span></span>
<span data-ttu-id="a76a7-154">A ID do recurso usado como a origem pelo monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a76a7-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="a76a7-155">-Marca</span><span class="sxs-lookup"><span data-stu-id="a76a7-155">-Tag</span></span>
<span data-ttu-id="a76a7-156">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a76a7-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a76a7-157">-The Test</span><span class="sxs-lookup"><span data-stu-id="a76a7-157">-TestGroup</span></span>
<span data-ttu-id="a76a7-158">A lista de grupos de teste.</span><span class="sxs-lookup"><span data-stu-id="a76a7-158">The list of test groups.</span></span>

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

### <span data-ttu-id="a76a7-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a76a7-159">-Confirm</span></span>
<span data-ttu-id="a76a7-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a76a7-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76a7-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76a7-161">-WhatIf</span></span>
<span data-ttu-id="a76a7-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a76a7-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76a7-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a76a7-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76a7-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76a7-164">CommonParameters</span></span>
<span data-ttu-id="a76a7-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76a7-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76a7-166">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a76a7-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76a7-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a76a7-167">INPUTS</span></span>

### <span data-ttu-id="a76a7-168">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a76a7-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a76a7-169">System. String</span><span class="sxs-lookup"><span data-stu-id="a76a7-169">System.String</span></span>

### <span data-ttu-id="a76a7-170">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a76a7-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a76a7-171">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a76a7-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a76a7-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a76a7-172">OUTPUTS</span></span>

### <span data-ttu-id="a76a7-173">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="a76a7-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="a76a7-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="a76a7-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="a76a7-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a76a7-175">NOTES</span></span>

## <span data-ttu-id="a76a7-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a76a7-176">RELATED LINKS</span></span>
