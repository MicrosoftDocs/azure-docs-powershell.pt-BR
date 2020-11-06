---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602923"
---
# <span data-ttu-id="e6052-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e6052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6052-102">SYNOPSIS</span></span>
<span data-ttu-id="e6052-103">Atualizar um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6052-104">SYNTAX</span></span>

### <span data-ttu-id="e6052-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6052-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6052-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e6052-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6052-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e6052-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6052-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6052-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6052-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6052-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6052-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6052-110">DESCRIPTION</span></span>
<span data-ttu-id="e6052-111">O cmdlet Set-AzureRmNetworkWatcherConnectionMonitor atualiza o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="e6052-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="e6052-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6052-112">EXAMPLES</span></span>

### <span data-ttu-id="e6052-113">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="e6052-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="e6052-114">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="e6052-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="e6052-115">OS</span><span class="sxs-lookup"><span data-stu-id="e6052-115">PARAMETERS</span></span>

### <span data-ttu-id="e6052-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6052-116">-AsJob</span></span>
<span data-ttu-id="e6052-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e6052-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6052-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="e6052-118">-ConfigureOnly</span></span>
<span data-ttu-id="e6052-119">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="e6052-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="e6052-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6052-120">-DefaultProfile</span></span>
<span data-ttu-id="e6052-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6052-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6052-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e6052-122">-DestinationAddress</span></span>
<span data-ttu-id="e6052-123">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e6052-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e6052-124">-DestinationPort</span></span>
<span data-ttu-id="e6052-125">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="e6052-125">Destination port.</span></span>

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

### <span data-ttu-id="e6052-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e6052-126">-DestinationResourceId</span></span>
<span data-ttu-id="e6052-127">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e6052-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6052-128">-InputObject</span></span>
<span data-ttu-id="e6052-129">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="e6052-130">-Local</span><span class="sxs-lookup"><span data-stu-id="e6052-130">-Location</span></span>
<span data-ttu-id="e6052-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e6052-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e6052-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e6052-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e6052-133">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="e6052-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="e6052-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6052-134">-Name</span></span>
<span data-ttu-id="e6052-135">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6052-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6052-136">-NetworkWatcher</span></span>
<span data-ttu-id="e6052-137">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e6052-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="e6052-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e6052-138">-NetworkWatcherName</span></span>
<span data-ttu-id="e6052-139">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e6052-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="e6052-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6052-140">-ResourceGroupName</span></span>
<span data-ttu-id="e6052-141">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e6052-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e6052-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6052-142">-ResourceId</span></span>
<span data-ttu-id="e6052-143">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e6052-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6052-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e6052-144">-SourcePort</span></span>
<span data-ttu-id="e6052-145">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="e6052-145">Source port.</span></span>

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

### <span data-ttu-id="e6052-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e6052-146">-SourceResourceId</span></span>
<span data-ttu-id="e6052-147">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="e6052-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="e6052-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="e6052-148">-Tag</span></span>
<span data-ttu-id="e6052-149">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6052-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e6052-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6052-150">-Confirm</span></span>
<span data-ttu-id="e6052-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6052-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6052-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6052-152">-WhatIf</span></span>
<span data-ttu-id="e6052-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6052-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6052-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6052-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6052-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6052-155">CommonParameters</span></span>
<span data-ttu-id="e6052-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6052-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6052-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6052-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6052-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6052-158">INPUTS</span></span>

### <span data-ttu-id="e6052-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6052-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e6052-160">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6052-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="e6052-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e6052-161">System.String</span></span>

### <span data-ttu-id="e6052-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e6052-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="e6052-163">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6052-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e6052-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6052-164">OUTPUTS</span></span>

### <span data-ttu-id="e6052-165">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e6052-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e6052-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6052-166">NOTES</span></span>
<span data-ttu-id="e6052-167">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="e6052-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e6052-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6052-168">RELATED LINKS</span></span>

[<span data-ttu-id="e6052-169">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6052-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e6052-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6052-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e6052-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e6052-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e6052-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e6052-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="e6052-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e6052-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="e6052-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e6052-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="e6052-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e6052-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="e6052-176">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6052-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e6052-177">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e6052-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="e6052-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6052-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e6052-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6052-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e6052-180">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6052-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e6052-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e6052-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="e6052-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-185">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-186">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-187">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6052-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="e6052-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e6052-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="e6052-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e6052-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="e6052-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e6052-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="e6052-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e6052-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e6052-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e6052-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="e6052-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e6052-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="e6052-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e6052-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="e6052-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e6052-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
