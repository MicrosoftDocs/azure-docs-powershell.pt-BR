---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 0d9d5867007c25db64cf8232ec9b66591362eef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885684"
---
# <span data-ttu-id="70865-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="70865-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="70865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70865-102">SYNOPSIS</span></span>
<span data-ttu-id="70865-103">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="70865-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="70865-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70865-104">SYNTAX</span></span>

### <span data-ttu-id="70865-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70865-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70865-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="70865-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70865-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="70865-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70865-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="70865-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70865-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70865-109">DESCRIPTION</span></span>
<span data-ttu-id="70865-110">O Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="70865-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="70865-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70865-111">EXAMPLES</span></span>

### <span data-ttu-id="70865-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70865-112">Example 1</span></span>
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

<span data-ttu-id="70865-113">Lista todos os provedores disponíveis em Seattle, WA para o Data Center do Azure no Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="70865-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="70865-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="70865-114">Example 2</span></span>

<span data-ttu-id="70865-115">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="70865-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="70865-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="70865-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="70865-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70865-117">PARAMETERS</span></span>

### <span data-ttu-id="70865-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70865-118">-AsJob</span></span>
<span data-ttu-id="70865-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="70865-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70865-120">-City</span><span class="sxs-lookup"><span data-stu-id="70865-120">-City</span></span>
<span data-ttu-id="70865-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="70865-121">The name of the city.</span></span>

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

### <span data-ttu-id="70865-122">-Country</span><span class="sxs-lookup"><span data-stu-id="70865-122">-Country</span></span>
<span data-ttu-id="70865-123">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="70865-123">The name of the country.</span></span>

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

### <span data-ttu-id="70865-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70865-124">-DefaultProfile</span></span>
<span data-ttu-id="70865-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="70865-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70865-126">-Location</span><span class="sxs-lookup"><span data-stu-id="70865-126">-Location</span></span>
<span data-ttu-id="70865-127">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="70865-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="70865-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70865-128">-NetworkWatcher</span></span>
<span data-ttu-id="70865-129">O recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="70865-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="70865-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="70865-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="70865-131">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="70865-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="70865-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="70865-132">-NetworkWatcherName</span></span>
<span data-ttu-id="70865-133">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="70865-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="70865-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70865-134">-ResourceGroupName</span></span>
<span data-ttu-id="70865-135">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="70865-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="70865-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70865-136">-ResourceId</span></span>
<span data-ttu-id="70865-137">A ID do recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="70865-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="70865-138">-State</span><span class="sxs-lookup"><span data-stu-id="70865-138">-State</span></span>
<span data-ttu-id="70865-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="70865-139">The name of the state.</span></span>

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

### <span data-ttu-id="70865-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70865-140">CommonParameters</span></span>
<span data-ttu-id="70865-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70865-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70865-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70865-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70865-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70865-143">INPUTS</span></span>

### <span data-ttu-id="70865-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70865-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="70865-145">System.String</span><span class="sxs-lookup"><span data-stu-id="70865-145">System.String</span></span>

## <span data-ttu-id="70865-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70865-146">OUTPUTS</span></span>

### <span data-ttu-id="70865-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="70865-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="70865-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="70865-148">NOTES</span></span>
<span data-ttu-id="70865-149">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="70865-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="70865-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70865-150">RELATED LINKS</span></span>

[<span data-ttu-id="70865-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70865-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="70865-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70865-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="70865-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70865-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="70865-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="70865-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="70865-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="70865-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="70865-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="70865-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="70865-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="70865-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="70865-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70865-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70865-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="70865-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="70865-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70865-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70865-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70865-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70865-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70865-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70865-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="70865-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="70865-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="70865-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="70865-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="70865-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="70865-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70865-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70865-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70865-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="70865-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="70865-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70865-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70865-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="70865-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="70865-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="70865-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="70865-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="70865-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="70865-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="70865-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="70865-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="70865-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="70865-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70865-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
