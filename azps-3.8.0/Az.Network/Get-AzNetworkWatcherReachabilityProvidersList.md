---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777678"
---
# <span data-ttu-id="29f62-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="29f62-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="29f62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29f62-102">SYNOPSIS</span></span>
<span data-ttu-id="29f62-103">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="29f62-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="29f62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29f62-104">SYNTAX</span></span>

### <span data-ttu-id="29f62-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="29f62-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f62-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29f62-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29f62-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29f62-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29f62-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29f62-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f62-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29f62-109">DESCRIPTION</span></span>
<span data-ttu-id="29f62-110">A Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="29f62-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="29f62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29f62-111">EXAMPLES</span></span>

### <span data-ttu-id="29f62-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29f62-112">Example 1</span></span>
```
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

<span data-ttu-id="29f62-113">Lista todos os provedores disponíveis em Seattle, WA para o Azure Data Center no oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="29f62-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="29f62-114">OS</span><span class="sxs-lookup"><span data-stu-id="29f62-114">PARAMETERS</span></span>

### <span data-ttu-id="29f62-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29f62-115">-AsJob</span></span>
<span data-ttu-id="29f62-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="29f62-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29f62-117">-Cidade</span><span class="sxs-lookup"><span data-stu-id="29f62-117">-City</span></span>
<span data-ttu-id="29f62-118">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="29f62-118">The name of the city.</span></span>

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

### <span data-ttu-id="29f62-119">-País</span><span class="sxs-lookup"><span data-stu-id="29f62-119">-Country</span></span>
<span data-ttu-id="29f62-120">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="29f62-120">The name of the country.</span></span>

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

### <span data-ttu-id="29f62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f62-121">-DefaultProfile</span></span>
<span data-ttu-id="29f62-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29f62-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f62-123">-Local</span><span class="sxs-lookup"><span data-stu-id="29f62-123">-Location</span></span>
<span data-ttu-id="29f62-124">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="29f62-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="29f62-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29f62-125">-NetworkWatcher</span></span>
<span data-ttu-id="29f62-126">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="29f62-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="29f62-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="29f62-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="29f62-128">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="29f62-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29f62-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29f62-129">-NetworkWatcherName</span></span>
<span data-ttu-id="29f62-130">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="29f62-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="29f62-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f62-131">-ResourceGroupName</span></span>
<span data-ttu-id="29f62-132">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="29f62-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="29f62-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29f62-133">-ResourceId</span></span>
<span data-ttu-id="29f62-134">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="29f62-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="29f62-135">-Estado</span><span class="sxs-lookup"><span data-stu-id="29f62-135">-State</span></span>
<span data-ttu-id="29f62-136">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="29f62-136">The name of the state.</span></span>

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

### <span data-ttu-id="29f62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f62-137">CommonParameters</span></span>
<span data-ttu-id="29f62-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f62-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f62-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29f62-140">INPUTS</span></span>

### <span data-ttu-id="29f62-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29f62-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="29f62-142">System. String</span><span class="sxs-lookup"><span data-stu-id="29f62-142">System.String</span></span>

## <span data-ttu-id="29f62-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29f62-143">OUTPUTS</span></span>

### <span data-ttu-id="29f62-144">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="29f62-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="29f62-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29f62-145">NOTES</span></span>
<span data-ttu-id="29f62-146">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="29f62-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="29f62-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29f62-147">RELATED LINKS</span></span>

[<span data-ttu-id="29f62-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29f62-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="29f62-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29f62-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="29f62-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29f62-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="29f62-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="29f62-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="29f62-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="29f62-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="29f62-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="29f62-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="29f62-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="29f62-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="29f62-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29f62-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29f62-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="29f62-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="29f62-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29f62-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29f62-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29f62-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29f62-159">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29f62-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29f62-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="29f62-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="29f62-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="29f62-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="29f62-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="29f62-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="29f62-163">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29f62-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29f62-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29f62-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="29f62-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="29f62-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29f62-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29f62-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="29f62-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="29f62-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="29f62-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="29f62-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="29f62-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="29f62-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="29f62-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="29f62-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="29f62-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="29f62-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29f62-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
