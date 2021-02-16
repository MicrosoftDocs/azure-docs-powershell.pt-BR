---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: e1b6b0339b093a048d6d74998ac6b0eb276e81cd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400275"
---
# <span data-ttu-id="d55dd-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d55dd-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="d55dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d55dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d55dd-103">Exibir as regras de grupo de segurança de rede configuradas e eficazes aplicadas em um VM.</span><span class="sxs-lookup"><span data-stu-id="d55dd-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d55dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d55dd-104">SYNTAX</span></span>

### <span data-ttu-id="d55dd-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d55dd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d55dd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d55dd-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d55dd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d55dd-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d55dd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d55dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d55dd-109">A Get-AzNetworkWatcherSecurityGroupView permite exibir as regras de grupo de segurança de rede configuradas e eficazes aplicadas em um VM.</span><span class="sxs-lookup"><span data-stu-id="d55dd-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d55dd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d55dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d55dd-111">Exemplo 1: Fazer uma chamada de Exibição de Grupo de Segurança em um VM</span><span class="sxs-lookup"><span data-stu-id="d55dd-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="d55dd-112">No exemplo acima, primeiro temos o Watcher de Rede regional e, em seguida, um VM na região.</span><span class="sxs-lookup"><span data-stu-id="d55dd-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="d55dd-113">Em seguida, fazemos uma chamada de Exibição de Grupo de Segurança no VM especificado.</span><span class="sxs-lookup"><span data-stu-id="d55dd-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="d55dd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d55dd-114">PARAMETERS</span></span>

### <span data-ttu-id="d55dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d55dd-115">-AsJob</span></span>
<span data-ttu-id="d55dd-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d55dd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d55dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55dd-117">-DefaultProfile</span></span>
<span data-ttu-id="d55dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d55dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d55dd-119">-Local</span><span class="sxs-lookup"><span data-stu-id="d55dd-119">-Location</span></span>
<span data-ttu-id="d55dd-120">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d55dd-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d55dd-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d55dd-121">-NetworkWatcher</span></span>
<span data-ttu-id="d55dd-122">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d55dd-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="d55dd-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d55dd-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d55dd-124">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d55dd-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d55dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="d55dd-126">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d55dd-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55dd-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d55dd-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d55dd-128">A ID do VM de destino</span><span class="sxs-lookup"><span data-stu-id="d55dd-128">The target VM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55dd-129">CommonParameters</span></span>
<span data-ttu-id="d55dd-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55dd-131">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d55dd-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55dd-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="d55dd-132">INPUTS</span></span>

### <span data-ttu-id="d55dd-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d55dd-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d55dd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d55dd-134">System.String</span></span>

## <span data-ttu-id="d55dd-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="d55dd-135">OUTPUTS</span></span>

### <span data-ttu-id="d55dd-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="d55dd-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="d55dd-137">Notas</span><span class="sxs-lookup"><span data-stu-id="d55dd-137">NOTES</span></span>
<span data-ttu-id="d55dd-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="d55dd-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d55dd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d55dd-139">RELATED LINKS</span></span>

[<span data-ttu-id="d55dd-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d55dd-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d55dd-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d55dd-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d55dd-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d55dd-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d55dd-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d55dd-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d55dd-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d55dd-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d55dd-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d55dd-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d55dd-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d55dd-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d55dd-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d55dd-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d55dd-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d55dd-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d55dd-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d55dd-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d55dd-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d55dd-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d55dd-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d55dd-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d55dd-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d55dd-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d55dd-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d55dd-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d55dd-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d55dd-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d55dd-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d55dd-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d55dd-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d55dd-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d55dd-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d55dd-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d55dd-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d55dd-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d55dd-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d55dd-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d55dd-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d55dd-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d55dd-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d55dd-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d55dd-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d55dd-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d55dd-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d55dd-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d55dd-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
