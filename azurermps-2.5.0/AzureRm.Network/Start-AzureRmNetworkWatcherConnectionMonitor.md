---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785453"
---
# <span data-ttu-id="51c1b-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51c1b-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="51c1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="51c1b-103">Iniciar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="51c1b-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51c1b-104">SYNTAX</span></span>

### <span data-ttu-id="51c1b-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="51c1b-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51c1b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="51c1b-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51c1b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="51c1b-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51c1b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51c1b-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51c1b-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="51c1b-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="51c1b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51c1b-110">DESCRIPTION</span></span>
<span data-ttu-id="51c1b-111">O cmdlet Start-AzureRmNetworkWatcherConnectionMonitor inicia o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="51c1b-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="51c1b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51c1b-112">EXAMPLES</span></span>

### <span data-ttu-id="51c1b-113">---------------Exemplo 1: iniciar um monitor de conexão---------------</span><span class="sxs-lookup"><span data-stu-id="51c1b-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="51c1b-114">Neste exemplo, começamos o monitor de conexão especificado por nome e Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="51c1b-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="51c1b-115">OS</span><span class="sxs-lookup"><span data-stu-id="51c1b-115">PARAMETERS</span></span>

### <span data-ttu-id="51c1b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51c1b-116">-AsJob</span></span>
<span data-ttu-id="51c1b-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51c1b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51c1b-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51c1b-118">-Confirm</span></span>
<span data-ttu-id="51c1b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51c1b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c1b-120">-DefaultProfile</span></span>
<span data-ttu-id="51c1b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51c1b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c1b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51c1b-122">-InputObject</span></span>
<span data-ttu-id="51c1b-123">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="51c1b-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="51c1b-124">-Local</span><span class="sxs-lookup"><span data-stu-id="51c1b-124">-Location</span></span>
<span data-ttu-id="51c1b-125">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="51c1b-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="51c1b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="51c1b-126">-Name</span></span>
<span data-ttu-id="51c1b-127">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="51c1b-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="51c1b-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51c1b-128">-NetworkWatcher</span></span>
<span data-ttu-id="51c1b-129">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="51c1b-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="51c1b-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="51c1b-130">-NetworkWatcherName</span></span>
<span data-ttu-id="51c1b-131">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="51c1b-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="51c1b-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51c1b-132">-PassThru</span></span>
<span data-ttu-id="51c1b-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="51c1b-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="51c1b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c1b-134">-ResourceGroupName</span></span>
<span data-ttu-id="51c1b-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="51c1b-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="51c1b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51c1b-136">-ResourceId</span></span>
<span data-ttu-id="51c1b-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="51c1b-137">Resource ID.</span></span>

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

### <span data-ttu-id="51c1b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c1b-138">-WhatIf</span></span>
<span data-ttu-id="51c1b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51c1b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51c1b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51c1b-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="51c1b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51c1b-141">INPUTS</span></span>

### <span data-ttu-id="51c1b-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51c1b-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="51c1b-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="51c1b-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="51c1b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51c1b-144">OUTPUTS</span></span>

### <span data-ttu-id="51c1b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51c1b-145">System.Boolean</span></span>


## <span data-ttu-id="51c1b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51c1b-146">NOTES</span></span>
<span data-ttu-id="51c1b-147">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="51c1b-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="51c1b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51c1b-148">RELATED LINKS</span></span>
<span data-ttu-id="51c1b-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="51c1b-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="51c1b-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="51c1b-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="51c1b-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="51c1b-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="51c1b-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Parar-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="51c1b-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
