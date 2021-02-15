---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 028af170e73397178dfe3b81ff216b7fdb0ecfe6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395666"
---
# <span data-ttu-id="51213-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="51213-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="51213-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51213-102">SYNOPSIS</span></span>
<span data-ttu-id="51213-103">Lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="51213-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="51213-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51213-104">SYNTAX</span></span>

### <span data-ttu-id="51213-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51213-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51213-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51213-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51213-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="51213-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51213-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51213-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51213-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="51213-109">DESCRIPTION</span></span>
<span data-ttu-id="51213-110">A Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="51213-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="51213-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51213-111">EXAMPLES</span></span>

### <span data-ttu-id="51213-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51213-112">Example 1</span></span>
```powershell
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="51213-113">Lista todos os provedores disponíveis em Seattle, WA para o Data Center do Azure no Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="51213-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="51213-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="51213-114">Example 2</span></span>

<span data-ttu-id="51213-115">Lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="51213-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="51213-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="51213-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="51213-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51213-117">PARAMETERS</span></span>

### <span data-ttu-id="51213-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51213-118">-AsJob</span></span>
<span data-ttu-id="51213-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51213-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51213-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="51213-120">-City</span></span>
<span data-ttu-id="51213-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="51213-121">The name of the city.</span></span>

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

### <span data-ttu-id="51213-122">-País/Região</span><span class="sxs-lookup"><span data-stu-id="51213-122">-Country</span></span>
<span data-ttu-id="51213-123">O nome do país/região.</span><span class="sxs-lookup"><span data-stu-id="51213-123">The name of the country.</span></span>

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

### <span data-ttu-id="51213-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51213-124">-DefaultProfile</span></span>
<span data-ttu-id="51213-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="51213-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51213-126">-Local</span><span class="sxs-lookup"><span data-stu-id="51213-126">-Location</span></span>
<span data-ttu-id="51213-127">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="51213-127">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51213-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51213-128">-NetworkWatcher</span></span>
<span data-ttu-id="51213-129">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="51213-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="51213-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="51213-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="51213-131">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="51213-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="51213-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="51213-132">-NetworkWatcherName</span></span>
<span data-ttu-id="51213-133">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="51213-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51213-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51213-134">-ResourceGroupName</span></span>
<span data-ttu-id="51213-135">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="51213-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="51213-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51213-136">-ResourceId</span></span>
<span data-ttu-id="51213-137">A ID do recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="51213-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="51213-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="51213-138">-State</span></span>
<span data-ttu-id="51213-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="51213-139">The name of the state.</span></span>

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

### <span data-ttu-id="51213-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51213-140">CommonParameters</span></span>
<span data-ttu-id="51213-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51213-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51213-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51213-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51213-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="51213-143">INPUTS</span></span>

### <span data-ttu-id="51213-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51213-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="51213-145">System.String</span><span class="sxs-lookup"><span data-stu-id="51213-145">System.String</span></span>

## <span data-ttu-id="51213-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="51213-146">OUTPUTS</span></span>

### <span data-ttu-id="51213-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="51213-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="51213-148">Notas</span><span class="sxs-lookup"><span data-stu-id="51213-148">NOTES</span></span>
<span data-ttu-id="51213-149">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="51213-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="51213-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51213-150">RELATED LINKS</span></span>

[<span data-ttu-id="51213-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51213-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="51213-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51213-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="51213-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51213-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="51213-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="51213-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="51213-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="51213-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="51213-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="51213-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="51213-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="51213-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="51213-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51213-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51213-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="51213-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="51213-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51213-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51213-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51213-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51213-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51213-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51213-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="51213-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="51213-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="51213-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="51213-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="51213-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="51213-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51213-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51213-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51213-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="51213-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="51213-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51213-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51213-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="51213-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="51213-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="51213-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="51213-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="51213-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="51213-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="51213-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="51213-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="51213-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="51213-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51213-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
