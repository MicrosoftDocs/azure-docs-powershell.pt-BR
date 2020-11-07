---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772760"
---
# <span data-ttu-id="18dbf-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="18dbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="18dbf-103">Atualizar um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-103">Update a connection monitor.</span></span>

## <span data-ttu-id="18dbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18dbf-104">SYNTAX</span></span>

### <span data-ttu-id="18dbf-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="18dbf-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18dbf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="18dbf-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18dbf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="18dbf-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18dbf-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="18dbf-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18dbf-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="18dbf-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18dbf-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18dbf-110">DESCRIPTION</span></span>
<span data-ttu-id="18dbf-111">O cmdlet Set-AzNetworkWatcherConnectionMonitor atualiza o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="18dbf-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="18dbf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18dbf-112">EXAMPLES</span></span>

### <span data-ttu-id="18dbf-113">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="18dbf-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="18dbf-114">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="18dbf-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="18dbf-115">OS</span><span class="sxs-lookup"><span data-stu-id="18dbf-115">PARAMETERS</span></span>

### <span data-ttu-id="18dbf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18dbf-116">-AsJob</span></span>
<span data-ttu-id="18dbf-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="18dbf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18dbf-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="18dbf-118">-ConfigureOnly</span></span>
<span data-ttu-id="18dbf-119">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="18dbf-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="18dbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dbf-120">-DefaultProfile</span></span>
<span data-ttu-id="18dbf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18dbf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18dbf-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="18dbf-122">-DestinationAddress</span></span>
<span data-ttu-id="18dbf-123">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="18dbf-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="18dbf-124">-DestinationPort</span></span>
<span data-ttu-id="18dbf-125">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="18dbf-125">Destination port.</span></span>

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

### <span data-ttu-id="18dbf-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="18dbf-126">-DestinationResourceId</span></span>
<span data-ttu-id="18dbf-127">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="18dbf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18dbf-128">-InputObject</span></span>
<span data-ttu-id="18dbf-129">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="18dbf-130">-Local</span><span class="sxs-lookup"><span data-stu-id="18dbf-130">-Location</span></span>
<span data-ttu-id="18dbf-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="18dbf-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="18dbf-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="18dbf-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="18dbf-133">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="18dbf-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="18dbf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="18dbf-134">-Name</span></span>
<span data-ttu-id="18dbf-135">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="18dbf-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18dbf-136">-NetworkWatcher</span></span>
<span data-ttu-id="18dbf-137">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="18dbf-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="18dbf-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="18dbf-138">-NetworkWatcherName</span></span>
<span data-ttu-id="18dbf-139">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="18dbf-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="18dbf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dbf-140">-ResourceGroupName</span></span>
<span data-ttu-id="18dbf-141">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="18dbf-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="18dbf-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18dbf-142">-ResourceId</span></span>
<span data-ttu-id="18dbf-143">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="18dbf-143">Resource ID.</span></span>

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

### <span data-ttu-id="18dbf-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="18dbf-144">-SourcePort</span></span>
<span data-ttu-id="18dbf-145">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="18dbf-145">Source port.</span></span>

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

### <span data-ttu-id="18dbf-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="18dbf-146">-SourceResourceId</span></span>
<span data-ttu-id="18dbf-147">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="18dbf-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="18dbf-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="18dbf-148">-Tag</span></span>
<span data-ttu-id="18dbf-149">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="18dbf-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="18dbf-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18dbf-150">-Confirm</span></span>
<span data-ttu-id="18dbf-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18dbf-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18dbf-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18dbf-152">-WhatIf</span></span>
<span data-ttu-id="18dbf-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18dbf-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18dbf-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18dbf-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18dbf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dbf-155">CommonParameters</span></span>
<span data-ttu-id="18dbf-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dbf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dbf-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18dbf-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dbf-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18dbf-158">INPUTS</span></span>

### <span data-ttu-id="18dbf-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18dbf-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="18dbf-160">System. String</span><span class="sxs-lookup"><span data-stu-id="18dbf-160">System.String</span></span>

### <span data-ttu-id="18dbf-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="18dbf-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="18dbf-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18dbf-162">OUTPUTS</span></span>

### <span data-ttu-id="18dbf-163">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="18dbf-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="18dbf-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18dbf-164">NOTES</span></span>
<span data-ttu-id="18dbf-165">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="18dbf-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="18dbf-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18dbf-166">RELATED LINKS</span></span>

[<span data-ttu-id="18dbf-167">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18dbf-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="18dbf-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18dbf-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="18dbf-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18dbf-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="18dbf-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="18dbf-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="18dbf-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="18dbf-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="18dbf-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="18dbf-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="18dbf-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="18dbf-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="18dbf-174">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18dbf-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18dbf-175">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="18dbf-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="18dbf-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18dbf-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18dbf-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18dbf-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18dbf-178">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18dbf-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18dbf-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="18dbf-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="18dbf-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-183">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-184">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-185">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="18dbf-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="18dbf-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="18dbf-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="18dbf-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="18dbf-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="18dbf-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="18dbf-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="18dbf-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18dbf-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18dbf-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="18dbf-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="18dbf-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="18dbf-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="18dbf-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="18dbf-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="18dbf-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="18dbf-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
