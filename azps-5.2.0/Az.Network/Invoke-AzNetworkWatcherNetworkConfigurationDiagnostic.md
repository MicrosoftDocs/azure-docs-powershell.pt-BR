---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 5a1500554c1026b591faea63074ca9c12fef1b10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264318"
---
# <span data-ttu-id="8e901-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e901-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="8e901-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e901-102">SYNOPSIS</span></span>
<span data-ttu-id="8e901-103">Invocar a sessão de diagnóstico de configuração de rede para os perfis de rede especificados no recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="8e901-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="8e901-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e901-104">SYNTAX</span></span>

### <span data-ttu-id="8e901-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e901-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e901-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8e901-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e901-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8e901-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e901-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e901-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e901-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e901-109">DESCRIPTION</span></span>
<span data-ttu-id="8e901-110">O cmdlet Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic invocar a sessão de diagnóstico de configuração de rede dos perfis de rede especificados no recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="8e901-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="8e901-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e901-111">EXAMPLES</span></span>

### <span data-ttu-id="8e901-112">Exemplo 1: invocar sessão de diagnóstico de configuração de rede para VM e perfil de rede especificado</span><span class="sxs-lookup"><span data-stu-id="8e901-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="8e901-113">OS</span><span class="sxs-lookup"><span data-stu-id="8e901-113">PARAMETERS</span></span>

### <span data-ttu-id="8e901-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e901-114">-AsJob</span></span>
<span data-ttu-id="8e901-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e901-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e901-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e901-116">-DefaultProfile</span></span>
<span data-ttu-id="8e901-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e901-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e901-118">-Local</span><span class="sxs-lookup"><span data-stu-id="8e901-118">-Location</span></span>
<span data-ttu-id="8e901-119">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8e901-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e901-120">-NetworkWatcher</span></span>
<span data-ttu-id="8e901-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="8e901-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8e901-122">-NetworkWatcherName</span></span>
<span data-ttu-id="8e901-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e901-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8e901-124">-Profile</span></span>
<span data-ttu-id="8e901-125">Lista de perfis de diagnóstico de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e901-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e901-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e901-127">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8e901-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e901-128">-ResourceId</span></span>
<span data-ttu-id="8e901-129">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8e901-129">Resource ID.</span></span>

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

### <span data-ttu-id="8e901-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8e901-130">-TargetResourceId</span></span>
<span data-ttu-id="8e901-131">A ID do recurso de destino para executar o diagnóstico de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="8e901-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="8e901-132">As opções válidas são VM, NetworkInterface, VMSS/NetworkInterface e Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8e901-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="8e901-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="8e901-133">-VerbosityLevel</span></span>
<span data-ttu-id="8e901-134">Nível de detalhamento.</span><span class="sxs-lookup"><span data-stu-id="8e901-134">Verbosity level.</span></span>
<span data-ttu-id="8e901-135">Os valores aceitos são ' normal ', ' Minimum ', ' full '.</span><span class="sxs-lookup"><span data-stu-id="8e901-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e901-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e901-136">CommonParameters</span></span>
<span data-ttu-id="8e901-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e901-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e901-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e901-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e901-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e901-139">INPUTS</span></span>

### <span data-ttu-id="8e901-140">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e901-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8e901-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8e901-141">System.String</span></span>

## <span data-ttu-id="8e901-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e901-142">OUTPUTS</span></span>

### <span data-ttu-id="8e901-143">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="8e901-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="8e901-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e901-144">NOTES</span></span>
<span data-ttu-id="8e901-145">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, diagnóstico, perfil</span><span class="sxs-lookup"><span data-stu-id="8e901-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="8e901-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e901-146">RELATED LINKS</span></span>

[<span data-ttu-id="8e901-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e901-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8e901-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e901-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8e901-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e901-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8e901-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8e901-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8e901-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8e901-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8e901-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8e901-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8e901-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8e901-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8e901-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e901-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e901-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8e901-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8e901-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e901-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e901-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e901-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e901-158">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e901-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e901-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e901-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8e901-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8e901-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8e901-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8e901-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8e901-162">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e901-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e901-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e901-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8e901-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8e901-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e901-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e901-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8e901-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8e901-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8e901-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8e901-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8e901-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8e901-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8e901-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8e901-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8e901-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8e901-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e901-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
