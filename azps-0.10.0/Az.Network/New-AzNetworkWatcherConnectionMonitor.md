---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775370"
---
# <span data-ttu-id="89803-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89803-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="89803-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89803-102">SYNOPSIS</span></span>
<span data-ttu-id="89803-103">Cria um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="89803-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="89803-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89803-104">SYNTAX</span></span>

### <span data-ttu-id="89803-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="89803-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89803-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="89803-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89803-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="89803-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="89803-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89803-108">DESCRIPTION</span></span>
<span data-ttu-id="89803-109">O cmdlet New-AzNetworkWatcherConnectionMonitor rcreates um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="89803-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="89803-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89803-110">EXAMPLES</span></span>

### <span data-ttu-id="89803-111">---------------Exemplo 1: criar um monitor de conexão para uma VM e um destino da Internet---------------</span><span class="sxs-lookup"><span data-stu-id="89803-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="89803-112">O cmdlet New-AzNetworkWatcherConnectionMonitor cria um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="89803-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="89803-113">OS</span><span class="sxs-lookup"><span data-stu-id="89803-113">PARAMETERS</span></span>

### <span data-ttu-id="89803-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89803-114">-AsJob</span></span>
<span data-ttu-id="89803-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89803-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89803-116">-Início do AutoStart</span><span class="sxs-lookup"><span data-stu-id="89803-116">-AutoStart</span></span>
<span data-ttu-id="89803-117">Início automático.</span><span class="sxs-lookup"><span data-stu-id="89803-117">Auto start.</span></span>

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

### <span data-ttu-id="89803-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89803-118">-Confirm</span></span>
<span data-ttu-id="89803-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89803-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89803-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89803-120">-DefaultProfile</span></span>
<span data-ttu-id="89803-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89803-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89803-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="89803-122">-DestinationAddress</span></span>
<span data-ttu-id="89803-123">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="89803-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="89803-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="89803-124">-DestinationPort</span></span>
<span data-ttu-id="89803-125">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="89803-125">Destination port.</span></span>

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

### <span data-ttu-id="89803-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="89803-126">-DestinationResourceId</span></span>
<span data-ttu-id="89803-127">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="89803-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="89803-128">-Force</span><span class="sxs-lookup"><span data-stu-id="89803-128">-Force</span></span>
<span data-ttu-id="89803-129">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="89803-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="89803-130">-Local</span><span class="sxs-lookup"><span data-stu-id="89803-130">-Location</span></span>
<span data-ttu-id="89803-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="89803-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="89803-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="89803-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="89803-133">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="89803-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="89803-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="89803-134">-Name</span></span>
<span data-ttu-id="89803-135">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="89803-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89803-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89803-136">-NetworkWatcher</span></span>
<span data-ttu-id="89803-137">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="89803-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="89803-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="89803-138">-NetworkWatcherName</span></span>
<span data-ttu-id="89803-139">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="89803-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="89803-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89803-140">-ResourceGroupName</span></span>
<span data-ttu-id="89803-141">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="89803-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="89803-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="89803-142">-SourcePort</span></span>
<span data-ttu-id="89803-143">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="89803-143">Source port.</span></span>

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

### <span data-ttu-id="89803-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="89803-144">-SourceResourceId</span></span>
<span data-ttu-id="89803-145">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="89803-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="89803-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="89803-146">-Tag</span></span>
<span data-ttu-id="89803-147">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="89803-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89803-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89803-148">-WhatIf</span></span>
<span data-ttu-id="89803-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89803-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89803-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89803-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="89803-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89803-151">INPUTS</span></span>

### <span data-ttu-id="89803-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89803-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="89803-153">System. String</span><span class="sxs-lookup"><span data-stu-id="89803-153">System.String</span></span>


## <span data-ttu-id="89803-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89803-154">OUTPUTS</span></span>

### <span data-ttu-id="89803-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="89803-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="89803-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89803-156">NOTES</span></span>
<span data-ttu-id="89803-157">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="89803-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="89803-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89803-158">RELATED LINKS</span></span>
<span data-ttu-id="89803-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="89803-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="89803-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="89803-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="89803-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Parar-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="89803-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="89803-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="89803-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
