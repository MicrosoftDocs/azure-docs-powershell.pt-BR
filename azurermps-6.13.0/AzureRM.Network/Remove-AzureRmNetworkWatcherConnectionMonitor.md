---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610274"
---
# <span data-ttu-id="afb4c-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="afb4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="afb4c-103">Remover o monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="afb4c-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afb4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afb4c-104">SYNTAX</span></span>

### <span data-ttu-id="afb4c-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="afb4c-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb4c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="afb4c-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb4c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="afb4c-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb4c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="afb4c-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb4c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="afb4c-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb4c-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afb4c-110">DESCRIPTION</span></span>
<span data-ttu-id="afb4c-111">O cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor remove o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="afb4c-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="afb4c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afb4c-112">EXAMPLES</span></span>

### <span data-ttu-id="afb4c-113">Exemplo 1: remover o monitor de conexão especificado</span><span class="sxs-lookup"><span data-stu-id="afb4c-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="afb4c-114">Neste exemplo, excluimos o monitor de conexão especificado por local e nome.</span><span class="sxs-lookup"><span data-stu-id="afb4c-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="afb4c-115">OS</span><span class="sxs-lookup"><span data-stu-id="afb4c-115">PARAMETERS</span></span>

### <span data-ttu-id="afb4c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afb4c-116">-AsJob</span></span>
<span data-ttu-id="afb4c-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="afb4c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afb4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb4c-118">-DefaultProfile</span></span>
<span data-ttu-id="afb4c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afb4c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb4c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afb4c-120">-InputObject</span></span>
<span data-ttu-id="afb4c-121">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="afb4c-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="afb4c-122">-Local</span><span class="sxs-lookup"><span data-stu-id="afb4c-122">-Location</span></span>
<span data-ttu-id="afb4c-123">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="afb4c-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="afb4c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="afb4c-124">-Name</span></span>
<span data-ttu-id="afb4c-125">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="afb4c-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="afb4c-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afb4c-126">-NetworkWatcher</span></span>
<span data-ttu-id="afb4c-127">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="afb4c-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="afb4c-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="afb4c-128">-NetworkWatcherName</span></span>
<span data-ttu-id="afb4c-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="afb4c-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="afb4c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb4c-130">-PassThru</span></span>
<span data-ttu-id="afb4c-131">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="afb4c-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="afb4c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb4c-132">-ResourceGroupName</span></span>
<span data-ttu-id="afb4c-133">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="afb4c-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="afb4c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb4c-134">-ResourceId</span></span>
<span data-ttu-id="afb4c-135">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="afb4c-135">Resource ID.</span></span>

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

### <span data-ttu-id="afb4c-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afb4c-136">-Confirm</span></span>
<span data-ttu-id="afb4c-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb4c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb4c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb4c-138">-WhatIf</span></span>
<span data-ttu-id="afb4c-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afb4c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb4c-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afb4c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb4c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb4c-141">CommonParameters</span></span>
<span data-ttu-id="afb4c-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb4c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb4c-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb4c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb4c-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afb4c-144">INPUTS</span></span>

### <span data-ttu-id="afb4c-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afb4c-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="afb4c-146">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="afb4c-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="afb4c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="afb4c-147">System.String</span></span>

### <span data-ttu-id="afb4c-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="afb4c-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="afb4c-149">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="afb4c-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="afb4c-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afb4c-150">OUTPUTS</span></span>

### <span data-ttu-id="afb4c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afb4c-151">System.Boolean</span></span>

## <span data-ttu-id="afb4c-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afb4c-152">NOTES</span></span>
<span data-ttu-id="afb4c-153">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="afb4c-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="afb4c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afb4c-154">RELATED LINKS</span></span>

[<span data-ttu-id="afb4c-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afb4c-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="afb4c-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afb4c-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="afb4c-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afb4c-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="afb4c-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="afb4c-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="afb4c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="afb4c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="afb4c-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="afb4c-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="afb4c-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="afb4c-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="afb4c-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afb4c-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="afb4c-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="afb4c-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="afb4c-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afb4c-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="afb4c-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afb4c-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="afb4c-166">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afb4c-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="afb4c-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="afb4c-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="afb4c-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-171">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="afb4c-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="afb4c-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="afb4c-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="afb4c-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="afb4c-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="afb4c-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="afb4c-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="afb4c-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afb4c-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="afb4c-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="afb4c-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="afb4c-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="afb4c-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="afb4c-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="afb4c-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="afb4c-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="afb4c-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
