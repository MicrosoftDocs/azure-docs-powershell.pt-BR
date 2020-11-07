---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: f40b7e28bce34ef9e4cc289bed7f8c4524ef49d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771723"
---
# <span data-ttu-id="b4d00-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4d00-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="b4d00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4d00-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d00-103">Exiba as regras de grupo de segurança de rede efetivas e configuradas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="b4d00-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b4d00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d00-104">SYNTAX</span></span>

### <span data-ttu-id="b4d00-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4d00-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d00-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b4d00-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d00-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b4d00-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d00-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4d00-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d00-109">O Get-AzNetworkWatcherSecurityGroupView permite que você veja as regras de grupo de segurança de rede configuradas e efetivas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="b4d00-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b4d00-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4d00-110">EXAMPLES</span></span>

### <span data-ttu-id="b4d00-111">Exemplo 1: fazer uma chamada de exibição de grupo de segurança em uma VM</span><span class="sxs-lookup"><span data-stu-id="b4d00-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="b4d00-112">No exemplo acima, obtemos primeiro o Inspetor de rede regional e, em seguida, uma VM na região.</span><span class="sxs-lookup"><span data-stu-id="b4d00-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="b4d00-113">Em seguida, fazemos uma chamada de exibição de grupo de segurança na VM especificada.</span><span class="sxs-lookup"><span data-stu-id="b4d00-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="b4d00-114">OS</span><span class="sxs-lookup"><span data-stu-id="b4d00-114">PARAMETERS</span></span>

### <span data-ttu-id="b4d00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4d00-115">-AsJob</span></span>
<span data-ttu-id="b4d00-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4d00-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4d00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d00-117">-DefaultProfile</span></span>
<span data-ttu-id="b4d00-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d00-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d00-119">-Local</span><span class="sxs-lookup"><span data-stu-id="b4d00-119">-Location</span></span>
<span data-ttu-id="b4d00-120">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b4d00-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b4d00-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4d00-121">-NetworkWatcher</span></span>
<span data-ttu-id="b4d00-122">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b4d00-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="b4d00-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b4d00-123">-NetworkWatcherName</span></span>
<span data-ttu-id="b4d00-124">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b4d00-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="b4d00-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d00-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4d00-126">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b4d00-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b4d00-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b4d00-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b4d00-128">A ID da VM de destino</span><span class="sxs-lookup"><span data-stu-id="b4d00-128">The target VM Id</span></span>

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

### <span data-ttu-id="b4d00-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d00-129">CommonParameters</span></span>
<span data-ttu-id="b4d00-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d00-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d00-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4d00-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d00-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4d00-132">INPUTS</span></span>

### <span data-ttu-id="b4d00-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4d00-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b4d00-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4d00-134">System.String</span></span>

## <span data-ttu-id="b4d00-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4d00-135">OUTPUTS</span></span>

### <span data-ttu-id="b4d00-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="b4d00-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="b4d00-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4d00-137">NOTES</span></span>
<span data-ttu-id="b4d00-138">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="b4d00-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="b4d00-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4d00-139">RELATED LINKS</span></span>

[<span data-ttu-id="b4d00-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4d00-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b4d00-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4d00-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b4d00-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4d00-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b4d00-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b4d00-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b4d00-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4d00-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b4d00-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b4d00-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b4d00-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b4d00-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b4d00-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4d00-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4d00-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b4d00-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b4d00-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4d00-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4d00-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4d00-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4d00-151">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4d00-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4d00-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4d00-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b4d00-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b4d00-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b4d00-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b4d00-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b4d00-155">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4d00-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4d00-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4d00-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b4d00-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b4d00-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4d00-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4d00-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b4d00-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b4d00-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4d00-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b4d00-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b4d00-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b4d00-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b4d00-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b4d00-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b4d00-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b4d00-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4d00-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
