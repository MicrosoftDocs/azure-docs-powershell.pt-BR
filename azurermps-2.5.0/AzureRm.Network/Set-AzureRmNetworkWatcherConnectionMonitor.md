---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785643"
---
# <span data-ttu-id="45b72-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45b72-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="45b72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45b72-102">SYNOPSIS</span></span>
<span data-ttu-id="45b72-103">Atualizar um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b72-104">SYNTAX</span></span>

### <span data-ttu-id="45b72-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="45b72-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45b72-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="45b72-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45b72-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="45b72-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45b72-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="45b72-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45b72-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="45b72-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="45b72-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45b72-110">DESCRIPTION</span></span>
<span data-ttu-id="45b72-111">O cmdlet Set-AzureRmNetworkWatcherConnectionMonitor atualiza o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="45b72-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="45b72-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45b72-112">EXAMPLES</span></span>

### <span data-ttu-id="45b72-113">---------------Exemplo 1: atualizar um monitor de conexão---------------</span><span class="sxs-lookup"><span data-stu-id="45b72-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="45b72-114">Neste exemplo, atualizamos o monitor de conexão existente alterando destinationAddress e adicionando marcas.</span><span class="sxs-lookup"><span data-stu-id="45b72-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="45b72-115">OS</span><span class="sxs-lookup"><span data-stu-id="45b72-115">PARAMETERS</span></span>

### <span data-ttu-id="45b72-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b72-116">-AsJob</span></span>
<span data-ttu-id="45b72-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45b72-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45b72-118">-Início do AutoStart</span><span class="sxs-lookup"><span data-stu-id="45b72-118">-AutoStart</span></span>
<span data-ttu-id="45b72-119">Início automático.</span><span class="sxs-lookup"><span data-stu-id="45b72-119">Auto start.</span></span>

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

### <span data-ttu-id="45b72-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45b72-120">-Confirm</span></span>
<span data-ttu-id="45b72-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b72-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b72-122">-DefaultProfile</span></span>
<span data-ttu-id="45b72-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45b72-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b72-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="45b72-124">-DestinationAddress</span></span>
<span data-ttu-id="45b72-125">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="45b72-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="45b72-126">-DestinationPort</span></span>
<span data-ttu-id="45b72-127">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="45b72-127">Destination port.</span></span>

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

### <span data-ttu-id="45b72-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="45b72-128">-DestinationResourceId</span></span>
<span data-ttu-id="45b72-129">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="45b72-130">-Force</span><span class="sxs-lookup"><span data-stu-id="45b72-130">-Force</span></span>
<span data-ttu-id="45b72-131">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="45b72-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="45b72-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45b72-132">-InputObject</span></span>
<span data-ttu-id="45b72-133">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="45b72-134">-Local</span><span class="sxs-lookup"><span data-stu-id="45b72-134">-Location</span></span>
<span data-ttu-id="45b72-135">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="45b72-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="45b72-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="45b72-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="45b72-137">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="45b72-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="45b72-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="45b72-138">-Name</span></span>
<span data-ttu-id="45b72-139">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="45b72-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45b72-140">-NetworkWatcher</span></span>
<span data-ttu-id="45b72-141">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="45b72-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="45b72-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="45b72-142">-NetworkWatcherName</span></span>
<span data-ttu-id="45b72-143">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="45b72-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="45b72-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b72-144">-ResourceGroupName</span></span>
<span data-ttu-id="45b72-145">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="45b72-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="45b72-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b72-146">-ResourceId</span></span>
<span data-ttu-id="45b72-147">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="45b72-147">Resource ID.</span></span>

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

### <span data-ttu-id="45b72-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="45b72-148">-SourcePort</span></span>
<span data-ttu-id="45b72-149">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="45b72-149">Source port.</span></span>

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

### <span data-ttu-id="45b72-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="45b72-150">-SourceResourceId</span></span>
<span data-ttu-id="45b72-151">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="45b72-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="45b72-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="45b72-152">-Tag</span></span>
<span data-ttu-id="45b72-153">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="45b72-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="45b72-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b72-154">-WhatIf</span></span>
<span data-ttu-id="45b72-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45b72-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b72-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45b72-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="45b72-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45b72-157">INPUTS</span></span>

### <span data-ttu-id="45b72-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45b72-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="45b72-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="45b72-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="45b72-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45b72-160">OUTPUTS</span></span>

### <span data-ttu-id="45b72-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="45b72-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="45b72-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45b72-162">NOTES</span></span>
<span data-ttu-id="45b72-163">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="45b72-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="45b72-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45b72-164">RELATED LINKS</span></span>
<span data-ttu-id="45b72-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="45b72-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="45b72-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="45b72-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="45b72-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="45b72-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="45b72-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="45b72-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

