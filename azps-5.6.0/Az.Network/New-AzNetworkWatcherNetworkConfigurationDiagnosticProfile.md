---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: 4efe4ea25260e8e17c35a8f85c9e521355f67300
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886185"
---
# <span data-ttu-id="4e12f-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="4e12f-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="4e12f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e12f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e12f-103">Cria um novo objeto de perfil de diagnóstico de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="4e12f-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="4e12f-104">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="4e12f-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="4e12f-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e12f-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e12f-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e12f-106">DESCRIPTION</span></span>
<span data-ttu-id="4e12f-107">O New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet cria um novo objeto de perfil de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4e12f-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="4e12f-108">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico de configuração de rede usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="4e12f-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="4e12f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e12f-109">EXAMPLES</span></span>

### <span data-ttu-id="4e12f-110">Exemplo 1: Invocar sessão de diagnóstico de configuração de rede para VM e perfil de rede especificado</span><span class="sxs-lookup"><span data-stu-id="4e12f-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="4e12f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e12f-111">PARAMETERS</span></span>

### <span data-ttu-id="4e12f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e12f-112">-DefaultProfile</span></span>
<span data-ttu-id="4e12f-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e12f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e12f-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="4e12f-114">-Destination</span></span>
<span data-ttu-id="4e12f-115">Destino do tráfego.</span><span class="sxs-lookup"><span data-stu-id="4e12f-115">Traffic destination.</span></span>
<span data-ttu-id="4e12f-116">Os valores aceitos são: '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="4e12f-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="4e12f-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4e12f-117">-DestinationPort</span></span>
<span data-ttu-id="4e12f-118">Porta de destino de tráfego.</span><span class="sxs-lookup"><span data-stu-id="4e12f-118">Traffic destination port.</span></span>
<span data-ttu-id="4e12f-119">Os valores aceitos são '\*', porta (por exemplo, 3389) e intervalo de portas (por exemplo, 80-100).</span><span class="sxs-lookup"><span data-stu-id="4e12f-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="4e12f-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="4e12f-120">-Direction</span></span>
<span data-ttu-id="4e12f-121">A direção do tráfego.</span><span class="sxs-lookup"><span data-stu-id="4e12f-121">The direction of the traffic.</span></span>
<span data-ttu-id="4e12f-122">Os valores aceitos são 'Entrada' e 'Saída'</span><span class="sxs-lookup"><span data-stu-id="4e12f-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e12f-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4e12f-123">-Protocol</span></span>
<span data-ttu-id="4e12f-124">Protocolo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="4e12f-124">Protocol to be verified on.</span></span>
<span data-ttu-id="4e12f-125">Os valores aceitos são '\*', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="4e12f-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="4e12f-126">-Source</span><span class="sxs-lookup"><span data-stu-id="4e12f-126">-Source</span></span>
<span data-ttu-id="4e12f-127">Fonte de tráfego.</span><span class="sxs-lookup"><span data-stu-id="4e12f-127">Traffic source.</span></span>
<span data-ttu-id="4e12f-128">Os valores aceitos são '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="4e12f-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="4e12f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e12f-129">CommonParameters</span></span>
<span data-ttu-id="4e12f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e12f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e12f-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e12f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e12f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e12f-132">INPUTS</span></span>

### <span data-ttu-id="4e12f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4e12f-133">System.String</span></span>

## <span data-ttu-id="4e12f-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e12f-134">OUTPUTS</span></span>

### <span data-ttu-id="4e12f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="4e12f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="4e12f-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e12f-136">NOTES</span></span>
<span data-ttu-id="4e12f-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="4e12f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="4e12f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e12f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e12f-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e12f-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4e12f-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e12f-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4e12f-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e12f-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4e12f-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4e12f-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4e12f-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4e12f-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4e12f-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4e12f-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4e12f-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4e12f-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4e12f-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e12f-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e12f-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4e12f-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4e12f-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e12f-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e12f-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e12f-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e12f-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e12f-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e12f-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e12f-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4e12f-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4e12f-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4e12f-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4e12f-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4e12f-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e12f-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e12f-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e12f-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e12f-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4e12f-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e12f-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e12f-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4e12f-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4e12f-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4e12f-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4e12f-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4e12f-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4e12f-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4e12f-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4e12f-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4e12f-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4e12f-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e12f-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
