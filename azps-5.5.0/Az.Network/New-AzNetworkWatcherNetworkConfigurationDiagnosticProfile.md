---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: e879de96f861c5a102077c3d392944f79a293b10
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398063"
---
# <span data-ttu-id="7ba95-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="7ba95-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="7ba95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ba95-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba95-103">Cria um novo objeto de perfil de diagnóstico de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="7ba95-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="7ba95-104">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="7ba95-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="7ba95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ba95-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba95-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ba95-106">DESCRIPTION</span></span>
<span data-ttu-id="7ba95-107">O New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet cria um novo objeto de perfil de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7ba95-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="7ba95-108">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico de configuração de rede usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="7ba95-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="7ba95-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ba95-109">EXAMPLES</span></span>

### <span data-ttu-id="7ba95-110">Exemplo 1: Sessão de diagnóstico de configuração de rede invocada para VM e perfil de rede especificado</span><span class="sxs-lookup"><span data-stu-id="7ba95-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="7ba95-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ba95-111">PARAMETERS</span></span>

### <span data-ttu-id="7ba95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba95-112">-DefaultProfile</span></span>
<span data-ttu-id="7ba95-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba95-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba95-114">-Destino</span><span class="sxs-lookup"><span data-stu-id="7ba95-114">-Destination</span></span>
<span data-ttu-id="7ba95-115">Destino do tráfego.</span><span class="sxs-lookup"><span data-stu-id="7ba95-115">Traffic destination.</span></span>
<span data-ttu-id="7ba95-116">Os valores aceitos são: '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="7ba95-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="7ba95-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7ba95-117">-DestinationPort</span></span>
<span data-ttu-id="7ba95-118">Porta de destino de tráfego.</span><span class="sxs-lookup"><span data-stu-id="7ba95-118">Traffic destination port.</span></span>
<span data-ttu-id="7ba95-119">Os valores aceitos são '\*', porta (por exemplo, 3389) e intervalo de portas (por exemplo, 80-100).</span><span class="sxs-lookup"><span data-stu-id="7ba95-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="7ba95-120">-Direção</span><span class="sxs-lookup"><span data-stu-id="7ba95-120">-Direction</span></span>
<span data-ttu-id="7ba95-121">A direção do tráfego.</span><span class="sxs-lookup"><span data-stu-id="7ba95-121">The direction of the traffic.</span></span>
<span data-ttu-id="7ba95-122">Os valores aceitos são "Entrada" e "Saída"</span><span class="sxs-lookup"><span data-stu-id="7ba95-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="7ba95-123">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="7ba95-123">-Protocol</span></span>
<span data-ttu-id="7ba95-124">Protocolo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="7ba95-124">Protocol to be verified on.</span></span>
<span data-ttu-id="7ba95-125">Os valores aceitos são '\*', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="7ba95-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="7ba95-126">-Origem</span><span class="sxs-lookup"><span data-stu-id="7ba95-126">-Source</span></span>
<span data-ttu-id="7ba95-127">Fonte de tráfego.</span><span class="sxs-lookup"><span data-stu-id="7ba95-127">Traffic source.</span></span>
<span data-ttu-id="7ba95-128">Os valores aceitos são '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="7ba95-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="7ba95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba95-129">CommonParameters</span></span>
<span data-ttu-id="7ba95-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba95-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba95-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba95-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ba95-132">INPUTS</span></span>

### <span data-ttu-id="7ba95-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7ba95-133">System.String</span></span>

## <span data-ttu-id="7ba95-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ba95-134">OUTPUTS</span></span>

### <span data-ttu-id="7ba95-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="7ba95-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="7ba95-136">Notas</span><span class="sxs-lookup"><span data-stu-id="7ba95-136">NOTES</span></span>
<span data-ttu-id="7ba95-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="7ba95-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="7ba95-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ba95-138">RELATED LINKS</span></span>

[<span data-ttu-id="7ba95-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ba95-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7ba95-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ba95-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7ba95-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ba95-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7ba95-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ba95-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7ba95-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ba95-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ba95-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7ba95-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7ba95-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ba95-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7ba95-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ba95-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ba95-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ba95-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ba95-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ba95-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ba95-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ba95-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ba95-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ba95-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ba95-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ba95-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7ba95-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ba95-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ba95-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7ba95-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7ba95-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ba95-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ba95-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ba95-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7ba95-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7ba95-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ba95-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ba95-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ba95-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7ba95-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7ba95-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7ba95-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7ba95-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7ba95-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7ba95-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7ba95-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7ba95-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7ba95-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ba95-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
