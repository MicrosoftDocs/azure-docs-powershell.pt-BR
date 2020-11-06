---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610108"
---
# <span data-ttu-id="69a10-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="69a10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69a10-102">SYNOPSIS</span></span>
<span data-ttu-id="69a10-103">Atualizar um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69a10-104">SYNTAX</span></span>

### <span data-ttu-id="69a10-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="69a10-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69a10-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="69a10-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69a10-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="69a10-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a10-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69a10-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a10-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="69a10-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a10-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69a10-110">DESCRIPTION</span></span>
<span data-ttu-id="69a10-111">O cmdlet Set-AzureRmNetworkWatcherConnectionMonitor atualiza o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="69a10-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="69a10-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69a10-112">EXAMPLES</span></span>

### <span data-ttu-id="69a10-113">Exemplo 1: atualizar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="69a10-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="69a10-114">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="69a10-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="69a10-115">OS</span><span class="sxs-lookup"><span data-stu-id="69a10-115">PARAMETERS</span></span>

### <span data-ttu-id="69a10-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69a10-116">-AsJob</span></span>
<span data-ttu-id="69a10-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69a10-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69a10-118">-Confirm</span></span>
<span data-ttu-id="69a10-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a10-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a10-120">-DefaultProfile</span></span>
<span data-ttu-id="69a10-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69a10-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="69a10-122">-DestinationAddress</span></span>
<span data-ttu-id="69a10-123">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="69a10-124">-DestinationPort</span></span>
<span data-ttu-id="69a10-125">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="69a10-125">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="69a10-126">-DestinationResourceId</span></span>
<span data-ttu-id="69a10-127">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69a10-128">-InputObject</span></span>
<span data-ttu-id="69a10-129">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-130">-Local</span><span class="sxs-lookup"><span data-stu-id="69a10-130">-Location</span></span>
<span data-ttu-id="69a10-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="69a10-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="69a10-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="69a10-133">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="69a10-133">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="69a10-134">-Name</span></span>
<span data-ttu-id="69a10-135">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69a10-136">-NetworkWatcher</span></span>
<span data-ttu-id="69a10-137">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="69a10-137">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="69a10-138">-NetworkWatcherName</span></span>
<span data-ttu-id="69a10-139">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="69a10-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a10-140">-ResourceGroupName</span></span>
<span data-ttu-id="69a10-141">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="69a10-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69a10-142">-ResourceId</span></span>
<span data-ttu-id="69a10-143">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="69a10-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="69a10-144">-SourcePort</span></span>
<span data-ttu-id="69a10-145">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="69a10-145">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="69a10-146">-SourceResourceId</span></span>
<span data-ttu-id="69a10-147">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="69a10-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="69a10-148">-Tag</span></span>
<span data-ttu-id="69a10-149">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="69a10-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a10-150">-WhatIf</span></span>
<span data-ttu-id="69a10-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69a10-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a10-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69a10-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="69a10-153">-ConfigureOnly</span></span>
<span data-ttu-id="69a10-154">Configurar o monitor de conexão, mas não iniciá-lo</span><span class="sxs-lookup"><span data-stu-id="69a10-154">Configure connection monitor, but do not start it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a10-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a10-155">CommonParameters</span></span>
<span data-ttu-id="69a10-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a10-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="69a10-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a10-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a10-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69a10-158">INPUTS</span></span>

### <span data-ttu-id="69a10-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69a10-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="69a10-160">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="69a10-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="69a10-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69a10-161">OUTPUTS</span></span>

### <span data-ttu-id="69a10-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="69a10-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="69a10-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69a10-163">NOTES</span></span>
<span data-ttu-id="69a10-164">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="69a10-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="69a10-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69a10-165">RELATED LINKS</span></span>

[<span data-ttu-id="69a10-166">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69a10-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69a10-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69a10-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69a10-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69a10-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69a10-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="69a10-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="69a10-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="69a10-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="69a10-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="69a10-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="69a10-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="69a10-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="69a10-173">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a10-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69a10-174">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="69a10-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="69a10-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a10-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69a10-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a10-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69a10-177">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69a10-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69a10-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69a10-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="69a10-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="69a10-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69a10-181">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69a10-182">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69a10-183">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69a10-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
