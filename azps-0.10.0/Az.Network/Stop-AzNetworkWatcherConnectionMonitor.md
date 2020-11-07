---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776484"
---
# <span data-ttu-id="f5db0-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5db0-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f5db0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5db0-102">SYNOPSIS</span></span>
<span data-ttu-id="f5db0-103">Parar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="f5db0-103">Stop a connection monitor</span></span>

## <span data-ttu-id="f5db0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5db0-104">SYNTAX</span></span>

### <span data-ttu-id="f5db0-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5db0-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5db0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f5db0-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5db0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f5db0-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5db0-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5db0-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5db0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5db0-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f5db0-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5db0-110">DESCRIPTION</span></span>
<span data-ttu-id="f5db0-111">O cmdlet Stop-AzNetworkWatcherConnectionMonitor interrompe o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="f5db0-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="f5db0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5db0-112">EXAMPLES</span></span>

### <span data-ttu-id="f5db0-113">---------------Exemplo 1: parar um monitor de conexão---------------</span><span class="sxs-lookup"><span data-stu-id="f5db0-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="f5db0-114">Neste exemplo, interrompemos o monitor de conexão especificado pelo nome e Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f5db0-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="f5db0-115">OS</span><span class="sxs-lookup"><span data-stu-id="f5db0-115">PARAMETERS</span></span>

### <span data-ttu-id="f5db0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5db0-116">-AsJob</span></span>
<span data-ttu-id="f5db0-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f5db0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5db0-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5db0-118">-Confirm</span></span>
<span data-ttu-id="f5db0-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5db0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5db0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5db0-120">-DefaultProfile</span></span>
<span data-ttu-id="f5db0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5db0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5db0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5db0-122">-InputObject</span></span>
<span data-ttu-id="f5db0-123">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="f5db0-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="f5db0-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f5db0-124">-Location</span></span>
<span data-ttu-id="f5db0-125">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f5db0-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f5db0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5db0-126">-Name</span></span>
<span data-ttu-id="f5db0-127">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="f5db0-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="f5db0-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5db0-128">-NetworkWatcher</span></span>
<span data-ttu-id="f5db0-129">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f5db0-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="f5db0-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f5db0-130">-NetworkWatcherName</span></span>
<span data-ttu-id="f5db0-131">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f5db0-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="f5db0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5db0-132">-PassThru</span></span>
<span data-ttu-id="f5db0-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f5db0-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f5db0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5db0-134">-ResourceGroupName</span></span>
<span data-ttu-id="f5db0-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f5db0-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f5db0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5db0-136">-ResourceId</span></span>
<span data-ttu-id="f5db0-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f5db0-137">Resource ID.</span></span>

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

### <span data-ttu-id="f5db0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5db0-138">-WhatIf</span></span>
<span data-ttu-id="f5db0-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5db0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5db0-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5db0-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f5db0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5db0-141">INPUTS</span></span>

### <span data-ttu-id="f5db0-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5db0-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f5db0-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f5db0-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f5db0-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5db0-144">OUTPUTS</span></span>

### <span data-ttu-id="f5db0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5db0-145">System.Boolean</span></span>


## <span data-ttu-id="f5db0-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5db0-146">NOTES</span></span>
<span data-ttu-id="f5db0-147">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="f5db0-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f5db0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5db0-148">RELATED LINKS</span></span>
<span data-ttu-id="f5db0-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f5db0-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="f5db0-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f5db0-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f5db0-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Parar-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f5db0-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="f5db0-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="f5db0-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>