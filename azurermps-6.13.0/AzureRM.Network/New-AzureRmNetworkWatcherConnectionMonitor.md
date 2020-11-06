---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7554183d52b263f4eed470295a2574a3d1f487b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441245"
---
# <span data-ttu-id="31b70-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="31b70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31b70-102">SYNOPSIS</span></span>
<span data-ttu-id="31b70-103">Cria um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="31b70-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31b70-104">SYNTAX</span></span>

### <span data-ttu-id="31b70-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="31b70-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b70-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="31b70-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b70-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="31b70-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b70-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31b70-108">DESCRIPTION</span></span>
<span data-ttu-id="31b70-109">O cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="31b70-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="31b70-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31b70-110">EXAMPLES</span></span>

### <span data-ttu-id="31b70-111">Exemplo 1: criar um monitor de conexão para uma VM e um destino da Internet</span><span class="sxs-lookup"><span data-stu-id="31b70-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="31b70-112">O cmdlet New-AzureRmNetworkWatcherConnectionMonitor cria um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="31b70-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="31b70-113">OS</span><span class="sxs-lookup"><span data-stu-id="31b70-113">PARAMETERS</span></span>

### <span data-ttu-id="31b70-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31b70-114">-AsJob</span></span>
<span data-ttu-id="31b70-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="31b70-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31b70-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="31b70-116">-ConfigureOnly</span></span>
<span data-ttu-id="31b70-117">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="31b70-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="31b70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b70-118">-DefaultProfile</span></span>
<span data-ttu-id="31b70-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31b70-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b70-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="31b70-120">-DestinationAddress</span></span>
<span data-ttu-id="31b70-121">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="31b70-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="31b70-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="31b70-122">-DestinationPort</span></span>
<span data-ttu-id="31b70-123">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="31b70-123">Destination port.</span></span>

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

### <span data-ttu-id="31b70-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="31b70-124">-DestinationResourceId</span></span>
<span data-ttu-id="31b70-125">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="31b70-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="31b70-126">-Force</span><span class="sxs-lookup"><span data-stu-id="31b70-126">-Force</span></span>
<span data-ttu-id="31b70-127">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="31b70-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="31b70-128">-Local</span><span class="sxs-lookup"><span data-stu-id="31b70-128">-Location</span></span>
<span data-ttu-id="31b70-129">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="31b70-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="31b70-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="31b70-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="31b70-131">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="31b70-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="31b70-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="31b70-132">-Name</span></span>
<span data-ttu-id="31b70-133">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="31b70-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="31b70-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31b70-134">-NetworkWatcher</span></span>
<span data-ttu-id="31b70-135">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="31b70-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="31b70-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="31b70-136">-NetworkWatcherName</span></span>
<span data-ttu-id="31b70-137">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="31b70-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="31b70-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b70-138">-ResourceGroupName</span></span>
<span data-ttu-id="31b70-139">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="31b70-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="31b70-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="31b70-140">-SourcePort</span></span>
<span data-ttu-id="31b70-141">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="31b70-141">Source port.</span></span>

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

### <span data-ttu-id="31b70-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="31b70-142">-SourceResourceId</span></span>
<span data-ttu-id="31b70-143">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="31b70-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="31b70-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="31b70-144">-Tag</span></span>
<span data-ttu-id="31b70-145">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="31b70-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="31b70-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31b70-146">-Confirm</span></span>
<span data-ttu-id="31b70-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b70-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b70-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b70-148">-WhatIf</span></span>
<span data-ttu-id="31b70-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31b70-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b70-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31b70-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b70-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b70-151">CommonParameters</span></span>
<span data-ttu-id="31b70-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b70-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b70-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b70-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b70-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31b70-154">INPUTS</span></span>

### <span data-ttu-id="31b70-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31b70-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="31b70-156">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31b70-156">Parameters: NetworkWatcher (ByValue)</span></span>

## <span data-ttu-id="31b70-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31b70-157">OUTPUTS</span></span>

### <span data-ttu-id="31b70-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="31b70-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="31b70-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31b70-159">NOTES</span></span>
<span data-ttu-id="31b70-160">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="31b70-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="31b70-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31b70-161">RELATED LINKS</span></span>

[<span data-ttu-id="31b70-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31b70-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="31b70-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31b70-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="31b70-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31b70-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="31b70-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="31b70-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="31b70-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="31b70-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="31b70-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="31b70-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="31b70-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="31b70-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="31b70-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31b70-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="31b70-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="31b70-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="31b70-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31b70-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="31b70-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31b70-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="31b70-173">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31b70-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="31b70-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="31b70-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="31b70-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-178">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-179">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-179">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-180">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="31b70-180">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="31b70-181">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="31b70-181">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="31b70-182">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="31b70-182">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="31b70-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="31b70-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="31b70-184">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31b70-184">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="31b70-185">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="31b70-185">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="31b70-186">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="31b70-186">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="31b70-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="31b70-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="31b70-188">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="31b70-188">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
