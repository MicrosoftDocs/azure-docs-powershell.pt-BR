---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116413"
---
# <span data-ttu-id="c344c-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c344c-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="c344c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c344c-102">SYNOPSIS</span></span>
<span data-ttu-id="c344c-103">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="c344c-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c344c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c344c-104">SYNTAX</span></span>

### <span data-ttu-id="c344c-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c344c-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c344c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c344c-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c344c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c344c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c344c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c344c-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c344c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c344c-109">DESCRIPTION</span></span>
<span data-ttu-id="c344c-110">A Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="c344c-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c344c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c344c-111">EXAMPLES</span></span>

### <span data-ttu-id="c344c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c344c-112">Example 1</span></span>
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

<span data-ttu-id="c344c-113">Lista todos os provedores disponíveis em Seattle, WA para o Azure Data Center no oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c344c-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="c344c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c344c-114">Example 2</span></span>

<span data-ttu-id="c344c-115">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="c344c-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="c344c-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="c344c-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="c344c-117">OS</span><span class="sxs-lookup"><span data-stu-id="c344c-117">PARAMETERS</span></span>

### <span data-ttu-id="c344c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c344c-118">-AsJob</span></span>
<span data-ttu-id="c344c-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c344c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c344c-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="c344c-120">-City</span></span>
<span data-ttu-id="c344c-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="c344c-121">The name of the city.</span></span>

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

### <span data-ttu-id="c344c-122">-País</span><span class="sxs-lookup"><span data-stu-id="c344c-122">-Country</span></span>
<span data-ttu-id="c344c-123">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="c344c-123">The name of the country.</span></span>

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

### <span data-ttu-id="c344c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c344c-124">-DefaultProfile</span></span>
<span data-ttu-id="c344c-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c344c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c344c-126">-Local</span><span class="sxs-lookup"><span data-stu-id="c344c-126">-Location</span></span>
<span data-ttu-id="c344c-127">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="c344c-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="c344c-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c344c-128">-NetworkWatcher</span></span>
<span data-ttu-id="c344c-129">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c344c-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="c344c-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c344c-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c344c-131">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c344c-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c344c-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c344c-132">-NetworkWatcherName</span></span>
<span data-ttu-id="c344c-133">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c344c-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="c344c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c344c-134">-ResourceGroupName</span></span>
<span data-ttu-id="c344c-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c344c-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c344c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c344c-136">-ResourceId</span></span>
<span data-ttu-id="c344c-137">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c344c-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c344c-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="c344c-138">-State</span></span>
<span data-ttu-id="c344c-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="c344c-139">The name of the state.</span></span>

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

### <span data-ttu-id="c344c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c344c-140">CommonParameters</span></span>
<span data-ttu-id="c344c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c344c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c344c-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c344c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c344c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c344c-143">INPUTS</span></span>

### <span data-ttu-id="c344c-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c344c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c344c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c344c-145">System.String</span></span>

## <span data-ttu-id="c344c-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c344c-146">OUTPUTS</span></span>

### <span data-ttu-id="c344c-147">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="c344c-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="c344c-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c344c-148">NOTES</span></span>
<span data-ttu-id="c344c-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="c344c-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c344c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c344c-150">RELATED LINKS</span></span>

[<span data-ttu-id="c344c-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c344c-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c344c-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c344c-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c344c-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c344c-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c344c-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c344c-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c344c-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c344c-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c344c-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c344c-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c344c-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c344c-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c344c-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c344c-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c344c-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c344c-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c344c-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c344c-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c344c-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c344c-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c344c-162">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c344c-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c344c-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c344c-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c344c-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c344c-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c344c-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c344c-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c344c-166">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c344c-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c344c-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c344c-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c344c-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c344c-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c344c-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c344c-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c344c-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c344c-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c344c-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c344c-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c344c-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c344c-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c344c-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c344c-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c344c-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c344c-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c344c-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
