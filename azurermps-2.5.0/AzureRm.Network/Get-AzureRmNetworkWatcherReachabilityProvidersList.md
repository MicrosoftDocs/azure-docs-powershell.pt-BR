---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
ms.openlocfilehash: c5a681f8be210e76ecbf3bc965e7e9e9c108a94a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785331"
---
# <span data-ttu-id="67ab2-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="67ab2-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="67ab2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="67ab2-103">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="67ab2-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67ab2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67ab2-104">SYNTAX</span></span>

### <span data-ttu-id="67ab2-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="67ab2-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ab2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="67ab2-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ab2-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="67ab2-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ab2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67ab2-108">DESCRIPTION</span></span>
<span data-ttu-id="67ab2-109">A Get-AzureRmNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="67ab2-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="67ab2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ab2-110">EXAMPLES</span></span>

### <span data-ttu-id="67ab2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67ab2-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="67ab2-112">Lista todos os provedores disponíveis em Seattle, WA para o Azure Data Center no oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="67ab2-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="67ab2-113">OS</span><span class="sxs-lookup"><span data-stu-id="67ab2-113">PARAMETERS</span></span>

### <span data-ttu-id="67ab2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67ab2-114">-AsJob</span></span>
<span data-ttu-id="67ab2-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="67ab2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-116">-Cidade</span><span class="sxs-lookup"><span data-stu-id="67ab2-116">-City</span></span>
<span data-ttu-id="67ab2-117">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="67ab2-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-118">-País</span><span class="sxs-lookup"><span data-stu-id="67ab2-118">-Country</span></span>
<span data-ttu-id="67ab2-119">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="67ab2-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ab2-120">-DefaultProfile</span></span>
<span data-ttu-id="67ab2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-122">-Local</span><span class="sxs-lookup"><span data-stu-id="67ab2-122">-Location</span></span>
<span data-ttu-id="67ab2-123">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="67ab2-123">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67ab2-124">-NetworkWatcher</span></span>
<span data-ttu-id="67ab2-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="67ab2-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="67ab2-126">-NetworkWatcherName</span></span>
<span data-ttu-id="67ab2-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="67ab2-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ab2-128">-ResourceGroupName</span></span>
<span data-ttu-id="67ab2-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="67ab2-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ab2-130">-ResourceId</span></span>
<span data-ttu-id="67ab2-131">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="67ab2-131">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="67ab2-132">-State</span></span>
<span data-ttu-id="67ab2-133">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="67ab2-133">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ab2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ab2-134">CommonParameters</span></span>
<span data-ttu-id="67ab2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ab2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ab2-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ab2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ab2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67ab2-137">INPUTS</span></span>

### <span data-ttu-id="67ab2-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67ab2-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="67ab2-139">System. String System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="67ab2-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="67ab2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67ab2-140">OUTPUTS</span></span>

### <span data-ttu-id="67ab2-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="67ab2-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="67ab2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67ab2-142">NOTES</span></span>
<span data-ttu-id="67ab2-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="67ab2-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="67ab2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ab2-144">RELATED LINKS</span></span>

[<span data-ttu-id="67ab2-145">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67ab2-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="67ab2-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67ab2-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="67ab2-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67ab2-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="67ab2-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="67ab2-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="67ab2-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="67ab2-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="67ab2-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="67ab2-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="67ab2-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="67ab2-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="67ab2-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67ab2-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67ab2-153">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="67ab2-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="67ab2-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67ab2-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67ab2-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67ab2-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67ab2-156">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67ab2-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
