---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771603"
---
# <span data-ttu-id="5977c-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5977c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5977c-102">SYNOPSIS</span></span>
<span data-ttu-id="5977c-103">Cria um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="5977c-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="5977c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5977c-104">SYNTAX</span></span>

### <span data-ttu-id="5977c-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5977c-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5977c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5977c-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5977c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5977c-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5977c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5977c-108">DESCRIPTION</span></span>
<span data-ttu-id="5977c-109">O cmdlet New-AzNetworkWatcherConnectionMonitor cria um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="5977c-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="5977c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5977c-110">EXAMPLES</span></span>

### <span data-ttu-id="5977c-111">Exemplo 1: criar um monitor de conexão para uma VM e um destino da Internet</span><span class="sxs-lookup"><span data-stu-id="5977c-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="5977c-112">O cmdlet New-AzNetworkWatcherConnectionMonitor cria um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="5977c-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="5977c-113">OS</span><span class="sxs-lookup"><span data-stu-id="5977c-113">PARAMETERS</span></span>

### <span data-ttu-id="5977c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5977c-114">-AsJob</span></span>
<span data-ttu-id="5977c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5977c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="5977c-116">-ConfigureOnly</span></span>
<span data-ttu-id="5977c-117">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="5977c-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="5977c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5977c-118">-DefaultProfile</span></span>
<span data-ttu-id="5977c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5977c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5977c-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5977c-120">-DestinationAddress</span></span>
<span data-ttu-id="5977c-121">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="5977c-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="5977c-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5977c-122">-DestinationPort</span></span>
<span data-ttu-id="5977c-123">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="5977c-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="5977c-124">-DestinationResourceId</span></span>
<span data-ttu-id="5977c-125">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="5977c-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="5977c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5977c-126">-Force</span></span>
<span data-ttu-id="5977c-127">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="5977c-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-128">-Local</span><span class="sxs-lookup"><span data-stu-id="5977c-128">-Location</span></span>
<span data-ttu-id="5977c-129">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5977c-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5977c-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5977c-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="5977c-131">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="5977c-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="5977c-132">-Name</span></span>
<span data-ttu-id="5977c-133">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="5977c-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="5977c-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5977c-134">-NetworkWatcher</span></span>
<span data-ttu-id="5977c-135">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5977c-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="5977c-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5977c-136">-NetworkWatcherName</span></span>
<span data-ttu-id="5977c-137">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5977c-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="5977c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5977c-138">-ResourceGroupName</span></span>
<span data-ttu-id="5977c-139">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="5977c-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5977c-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="5977c-140">-SourcePort</span></span>
<span data-ttu-id="5977c-141">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="5977c-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5977c-142">-SourceResourceId</span></span>
<span data-ttu-id="5977c-143">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="5977c-143">The ID of the connection monitor source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="5977c-144">-Tag</span></span>
<span data-ttu-id="5977c-145">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="5977c-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5977c-146">-Confirm</span></span>
<span data-ttu-id="5977c-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5977c-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5977c-148">-WhatIf</span></span>
<span data-ttu-id="5977c-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5977c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5977c-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5977c-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5977c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5977c-151">CommonParameters</span></span>
<span data-ttu-id="5977c-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5977c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5977c-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5977c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5977c-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5977c-154">INPUTS</span></span>

### <span data-ttu-id="5977c-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5977c-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5977c-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5977c-156">OUTPUTS</span></span>

### <span data-ttu-id="5977c-157">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="5977c-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="5977c-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5977c-158">NOTES</span></span>
<span data-ttu-id="5977c-159">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="5977c-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="5977c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5977c-160">RELATED LINKS</span></span>

[<span data-ttu-id="5977c-161">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5977c-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5977c-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5977c-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5977c-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5977c-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5977c-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5977c-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5977c-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5977c-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5977c-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5977c-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5977c-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5977c-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5977c-168">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5977c-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5977c-169">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5977c-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5977c-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5977c-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5977c-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5977c-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5977c-172">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5977c-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5977c-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5977c-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5977c-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-177">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-178">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-179">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5977c-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5977c-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5977c-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5977c-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5977c-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5977c-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5977c-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5977c-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5977c-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5977c-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5977c-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5977c-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5977c-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5977c-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5977c-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5977c-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5977c-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
