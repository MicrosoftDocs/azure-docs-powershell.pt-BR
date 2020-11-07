---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776521"
---
# <span data-ttu-id="73dfe-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="73dfe-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="73dfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="73dfe-103">Atualizar um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-103">Update a connection monitor.</span></span>

## <span data-ttu-id="73dfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73dfe-104">SYNTAX</span></span>

### <span data-ttu-id="73dfe-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="73dfe-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73dfe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="73dfe-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73dfe-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="73dfe-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73dfe-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73dfe-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73dfe-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="73dfe-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="73dfe-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73dfe-110">DESCRIPTION</span></span>
<span data-ttu-id="73dfe-111">O cmdlet Set-AzNetworkWatcherConnectionMonitor atualiza o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="73dfe-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="73dfe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73dfe-112">EXAMPLES</span></span>

### <span data-ttu-id="73dfe-113">---------------Exemplo 1: atualizar um monitor de conexão---------------</span><span class="sxs-lookup"><span data-stu-id="73dfe-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="73dfe-114">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="73dfe-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="73dfe-115">OS</span><span class="sxs-lookup"><span data-stu-id="73dfe-115">PARAMETERS</span></span>

### <span data-ttu-id="73dfe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73dfe-116">-AsJob</span></span>
<span data-ttu-id="73dfe-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="73dfe-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73dfe-118">-Início do AutoStart</span><span class="sxs-lookup"><span data-stu-id="73dfe-118">-AutoStart</span></span>
<span data-ttu-id="73dfe-119">Início automático.</span><span class="sxs-lookup"><span data-stu-id="73dfe-119">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73dfe-120">-Confirm</span></span>
<span data-ttu-id="73dfe-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73dfe-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73dfe-122">-DefaultProfile</span></span>
<span data-ttu-id="73dfe-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73dfe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73dfe-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="73dfe-124">-DestinationAddress</span></span>
<span data-ttu-id="73dfe-125">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="73dfe-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="73dfe-126">-DestinationPort</span></span>
<span data-ttu-id="73dfe-127">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="73dfe-127">Destination port.</span></span>

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

### <span data-ttu-id="73dfe-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="73dfe-128">-DestinationResourceId</span></span>
<span data-ttu-id="73dfe-129">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="73dfe-130">-Force</span><span class="sxs-lookup"><span data-stu-id="73dfe-130">-Force</span></span>
<span data-ttu-id="73dfe-131">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="73dfe-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="73dfe-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73dfe-132">-InputObject</span></span>
<span data-ttu-id="73dfe-133">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-134">-Local</span><span class="sxs-lookup"><span data-stu-id="73dfe-134">-Location</span></span>
<span data-ttu-id="73dfe-135">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="73dfe-135">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="73dfe-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="73dfe-137">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="73dfe-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="73dfe-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="73dfe-138">-Name</span></span>
<span data-ttu-id="73dfe-139">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="73dfe-140">-NetworkWatcher</span></span>
<span data-ttu-id="73dfe-141">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="73dfe-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="73dfe-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="73dfe-142">-NetworkWatcherName</span></span>
<span data-ttu-id="73dfe-143">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="73dfe-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73dfe-144">-ResourceGroupName</span></span>
<span data-ttu-id="73dfe-145">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="73dfe-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73dfe-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73dfe-146">-ResourceId</span></span>
<span data-ttu-id="73dfe-147">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="73dfe-147">Resource ID.</span></span>

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

### <span data-ttu-id="73dfe-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="73dfe-148">-SourcePort</span></span>
<span data-ttu-id="73dfe-149">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="73dfe-149">Source port.</span></span>

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

### <span data-ttu-id="73dfe-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="73dfe-150">-SourceResourceId</span></span>
<span data-ttu-id="73dfe-151">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="73dfe-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="73dfe-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="73dfe-152">-Tag</span></span>
<span data-ttu-id="73dfe-153">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="73dfe-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="73dfe-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73dfe-154">-WhatIf</span></span>
<span data-ttu-id="73dfe-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73dfe-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73dfe-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73dfe-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="73dfe-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73dfe-157">INPUTS</span></span>

### <span data-ttu-id="73dfe-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="73dfe-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="73dfe-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="73dfe-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="73dfe-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73dfe-160">OUTPUTS</span></span>

### <span data-ttu-id="73dfe-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="73dfe-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="73dfe-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73dfe-162">NOTES</span></span>
<span data-ttu-id="73dfe-163">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="73dfe-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="73dfe-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73dfe-164">RELATED LINKS</span></span>
<span data-ttu-id="73dfe-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="73dfe-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="73dfe-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="73dfe-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="73dfe-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Parar-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="73dfe-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="73dfe-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="73dfe-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

