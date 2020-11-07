---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785892"
---
# <span data-ttu-id="3df2c-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3df2c-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3df2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3df2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3df2c-103">Cria um monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3df2c-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3df2c-104">SYNTAX</span></span>

### <span data-ttu-id="3df2c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3df2c-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3df2c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3df2c-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3df2c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3df2c-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3df2c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3df2c-108">DESCRIPTION</span></span>
<span data-ttu-id="3df2c-109">O cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="3df2c-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="3df2c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3df2c-110">EXAMPLES</span></span>

### <span data-ttu-id="3df2c-111">---------------Exemplo 1: criar um monitor de conexão para uma VM e um destino da Internet---------------</span><span class="sxs-lookup"><span data-stu-id="3df2c-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="3df2c-112">O cmdlet New-AzureRmNetworkWatcherConnectionMonitor cria um monitor de conexão para uma origem e um destino especificados.</span><span class="sxs-lookup"><span data-stu-id="3df2c-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="3df2c-113">OS</span><span class="sxs-lookup"><span data-stu-id="3df2c-113">PARAMETERS</span></span>

### <span data-ttu-id="3df2c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3df2c-114">-AsJob</span></span>
<span data-ttu-id="3df2c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3df2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3df2c-116">-Início do AutoStart</span><span class="sxs-lookup"><span data-stu-id="3df2c-116">-AutoStart</span></span>
<span data-ttu-id="3df2c-117">Início automático.</span><span class="sxs-lookup"><span data-stu-id="3df2c-117">Auto start.</span></span>

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

### <span data-ttu-id="3df2c-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3df2c-118">-Confirm</span></span>
<span data-ttu-id="3df2c-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df2c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df2c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df2c-120">-DefaultProfile</span></span>
<span data-ttu-id="3df2c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3df2c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df2c-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3df2c-122">-DestinationAddress</span></span>
<span data-ttu-id="3df2c-123">O endereço IP do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3df2c-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3df2c-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3df2c-124">-DestinationPort</span></span>
<span data-ttu-id="3df2c-125">Porta de destino.</span><span class="sxs-lookup"><span data-stu-id="3df2c-125">Destination port.</span></span>

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

### <span data-ttu-id="3df2c-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="3df2c-126">-DestinationResourceId</span></span>
<span data-ttu-id="3df2c-127">A ID do destino do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3df2c-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3df2c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="3df2c-128">-Force</span></span>
<span data-ttu-id="3df2c-129">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="3df2c-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3df2c-130">-Local</span><span class="sxs-lookup"><span data-stu-id="3df2c-130">-Location</span></span>
<span data-ttu-id="3df2c-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3df2c-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3df2c-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3df2c-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="3df2c-133">Intervalo de monitoramento em segundos.</span><span class="sxs-lookup"><span data-stu-id="3df2c-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="3df2c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3df2c-134">-Name</span></span>
<span data-ttu-id="3df2c-135">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3df2c-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="3df2c-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3df2c-136">-NetworkWatcher</span></span>
<span data-ttu-id="3df2c-137">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3df2c-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="3df2c-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3df2c-138">-NetworkWatcherName</span></span>
<span data-ttu-id="3df2c-139">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3df2c-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="3df2c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df2c-140">-ResourceGroupName</span></span>
<span data-ttu-id="3df2c-141">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3df2c-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3df2c-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3df2c-142">-SourcePort</span></span>
<span data-ttu-id="3df2c-143">Porta de origem.</span><span class="sxs-lookup"><span data-stu-id="3df2c-143">Source port.</span></span>

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

### <span data-ttu-id="3df2c-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3df2c-144">-SourceResourceId</span></span>
<span data-ttu-id="3df2c-145">A ID da fonte do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3df2c-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="3df2c-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="3df2c-146">-Tag</span></span>
<span data-ttu-id="3df2c-147">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="3df2c-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3df2c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df2c-148">-WhatIf</span></span>
<span data-ttu-id="3df2c-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3df2c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df2c-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3df2c-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="3df2c-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3df2c-151">INPUTS</span></span>

### <span data-ttu-id="3df2c-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3df2c-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3df2c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3df2c-153">System.String</span></span>


## <span data-ttu-id="3df2c-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3df2c-154">OUTPUTS</span></span>

### <span data-ttu-id="3df2c-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3df2c-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="3df2c-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3df2c-156">NOTES</span></span>
<span data-ttu-id="3df2c-157">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="3df2c-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3df2c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3df2c-158">RELATED LINKS</span></span>
<span data-ttu-id="3df2c-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="3df2c-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="3df2c-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="3df2c-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="3df2c-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="3df2c-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="3df2c-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="3df2c-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
