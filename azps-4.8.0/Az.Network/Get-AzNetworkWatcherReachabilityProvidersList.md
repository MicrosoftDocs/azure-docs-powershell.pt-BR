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
ms.locfileid: "100402500"
---
# <span data-ttu-id="d4c19-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d4c19-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="d4c19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4c19-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c19-103">Lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c19-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d4c19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4c19-104">SYNTAX</span></span>

### <span data-ttu-id="d4c19-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4c19-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4c19-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d4c19-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c19-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d4c19-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c19-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4c19-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4c19-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4c19-109">DESCRIPTION</span></span>
<span data-ttu-id="d4c19-110">A Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c19-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d4c19-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4c19-111">EXAMPLES</span></span>

### <span data-ttu-id="d4c19-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4c19-112">Example 1</span></span>
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

<span data-ttu-id="d4c19-113">Lista todos os provedores disponíveis em Seattle, WA para o Data Center do Azure no Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d4c19-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="d4c19-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d4c19-114">Example 2</span></span>

<span data-ttu-id="d4c19-115">Lista todos os provedores de serviços de Internet disponíveis para uma região especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c19-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="d4c19-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d4c19-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="d4c19-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4c19-117">PARAMETERS</span></span>

### <span data-ttu-id="d4c19-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c19-118">-AsJob</span></span>
<span data-ttu-id="d4c19-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d4c19-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4c19-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="d4c19-120">-City</span></span>
<span data-ttu-id="d4c19-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="d4c19-121">The name of the city.</span></span>

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

### <span data-ttu-id="d4c19-122">-País/Região</span><span class="sxs-lookup"><span data-stu-id="d4c19-122">-Country</span></span>
<span data-ttu-id="d4c19-123">O nome do país/região.</span><span class="sxs-lookup"><span data-stu-id="d4c19-123">The name of the country.</span></span>

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

### <span data-ttu-id="d4c19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c19-124">-DefaultProfile</span></span>
<span data-ttu-id="d4c19-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d4c19-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c19-126">-Local</span><span class="sxs-lookup"><span data-stu-id="d4c19-126">-Location</span></span>
<span data-ttu-id="d4c19-127">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="d4c19-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="d4c19-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c19-128">-NetworkWatcher</span></span>
<span data-ttu-id="d4c19-129">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d4c19-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="d4c19-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="d4c19-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="d4c19-131">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d4c19-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d4c19-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d4c19-132">-NetworkWatcherName</span></span>
<span data-ttu-id="d4c19-133">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d4c19-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="d4c19-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c19-134">-ResourceGroupName</span></span>
<span data-ttu-id="d4c19-135">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d4c19-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d4c19-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4c19-136">-ResourceId</span></span>
<span data-ttu-id="d4c19-137">A ID do recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="d4c19-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="d4c19-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="d4c19-138">-State</span></span>
<span data-ttu-id="d4c19-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="d4c19-139">The name of the state.</span></span>

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

### <span data-ttu-id="d4c19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c19-140">CommonParameters</span></span>
<span data-ttu-id="d4c19-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c19-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4c19-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c19-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="d4c19-143">INPUTS</span></span>

### <span data-ttu-id="d4c19-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c19-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d4c19-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d4c19-145">System.String</span></span>

## <span data-ttu-id="d4c19-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="d4c19-146">OUTPUTS</span></span>

### <span data-ttu-id="d4c19-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="d4c19-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="d4c19-148">Notas</span><span class="sxs-lookup"><span data-stu-id="d4c19-148">NOTES</span></span>
<span data-ttu-id="d4c19-149">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="d4c19-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d4c19-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4c19-150">RELATED LINKS</span></span>

[<span data-ttu-id="d4c19-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c19-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d4c19-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c19-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d4c19-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4c19-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d4c19-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d4c19-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d4c19-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d4c19-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d4c19-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d4c19-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d4c19-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d4c19-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d4c19-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c19-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c19-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d4c19-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d4c19-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c19-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c19-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c19-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c19-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4c19-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4c19-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4c19-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d4c19-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d4c19-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d4c19-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d4c19-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d4c19-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c19-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c19-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c19-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d4c19-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d4c19-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c19-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4c19-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d4c19-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d4c19-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d4c19-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d4c19-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d4c19-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d4c19-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d4c19-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d4c19-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d4c19-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d4c19-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4c19-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
