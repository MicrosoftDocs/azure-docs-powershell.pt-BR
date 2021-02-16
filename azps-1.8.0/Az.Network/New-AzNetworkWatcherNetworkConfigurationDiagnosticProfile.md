---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: f406ddbf3e975e6caa3d9e9164673ec95a311e76
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400171"
---
# <span data-ttu-id="01b90-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="01b90-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="01b90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01b90-102">SYNOPSIS</span></span>
<span data-ttu-id="01b90-103">Cria um novo objeto de perfil de diagnóstico de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="01b90-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="01b90-104">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="01b90-104">This object is used to restrict the network confiuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="01b90-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01b90-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01b90-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="01b90-106">DESCRIPTION</span></span>
<span data-ttu-id="01b90-107">O New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet cria um novo objeto de perfil de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="01b90-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="01b90-108">Esse objeto é usado para restringir a configuração de rede durante uma sessão de diagnóstico de configuração de rede usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="01b90-108">This object is used to restrict the network confiuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="01b90-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01b90-109">EXAMPLES</span></span>

### <span data-ttu-id="01b90-110">Exemplo 1: Sessão de diagnóstico de configuração de rede invocada para VM e perfil de rede especificado</span><span class="sxs-lookup"><span data-stu-id="01b90-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="01b90-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01b90-111">PARAMETERS</span></span>

### <span data-ttu-id="01b90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b90-112">-DefaultProfile</span></span>
<span data-ttu-id="01b90-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01b90-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b90-114">-Destino</span><span class="sxs-lookup"><span data-stu-id="01b90-114">-Destination</span></span>
<span data-ttu-id="01b90-115">Destino do tráfego.</span><span class="sxs-lookup"><span data-stu-id="01b90-115">Traffic destination.</span></span>
<span data-ttu-id="01b90-116">Os valores aceitos são: '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="01b90-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="01b90-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="01b90-117">-DestinationPort</span></span>
<span data-ttu-id="01b90-118">Porta de destino de tráfego.</span><span class="sxs-lookup"><span data-stu-id="01b90-118">Traffic destination port.</span></span>
<span data-ttu-id="01b90-119">Os valores aceitos são '\*', porta (por exemplo, 3389) e intervalo de portas (por exemplo, 80-100).</span><span class="sxs-lookup"><span data-stu-id="01b90-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="01b90-120">-Direção</span><span class="sxs-lookup"><span data-stu-id="01b90-120">-Direction</span></span>
<span data-ttu-id="01b90-121">A direção do tráfego.</span><span class="sxs-lookup"><span data-stu-id="01b90-121">The direction of the traffic.</span></span>
<span data-ttu-id="01b90-122">Os valores aceitos são "Entrada" e "Saída"</span><span class="sxs-lookup"><span data-stu-id="01b90-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="01b90-123">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="01b90-123">-Protocol</span></span>
<span data-ttu-id="01b90-124">Protocolo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="01b90-124">Protocol to be verified on.</span></span>
<span data-ttu-id="01b90-125">Os valores aceitos são '\*', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="01b90-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="01b90-126">-Origem</span><span class="sxs-lookup"><span data-stu-id="01b90-126">-Source</span></span>
<span data-ttu-id="01b90-127">Fonte de tráfego.</span><span class="sxs-lookup"><span data-stu-id="01b90-127">Traffic source.</span></span>
<span data-ttu-id="01b90-128">Os valores aceitos são '\*', Endereço IP/CIDR, Marca de Serviço.</span><span class="sxs-lookup"><span data-stu-id="01b90-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="01b90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b90-129">CommonParameters</span></span>
<span data-ttu-id="01b90-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b90-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01b90-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b90-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="01b90-132">INPUTS</span></span>

### <span data-ttu-id="01b90-133">System.String</span><span class="sxs-lookup"><span data-stu-id="01b90-133">System.String</span></span>

## <span data-ttu-id="01b90-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="01b90-134">OUTPUTS</span></span>

### <span data-ttu-id="01b90-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="01b90-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="01b90-136">Notas</span><span class="sxs-lookup"><span data-stu-id="01b90-136">NOTES</span></span>
<span data-ttu-id="01b90-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="01b90-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="01b90-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01b90-138">RELATED LINKS</span></span>

[<span data-ttu-id="01b90-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="01b90-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="01b90-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="01b90-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="01b90-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="01b90-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="01b90-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="01b90-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="01b90-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="01b90-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="01b90-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="01b90-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="01b90-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="01b90-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="01b90-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="01b90-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="01b90-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="01b90-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="01b90-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="01b90-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="01b90-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="01b90-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="01b90-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="01b90-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="01b90-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="01b90-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="01b90-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="01b90-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="01b90-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
