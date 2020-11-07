---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775505"
---
# <span data-ttu-id="ddbdb-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ddbdb-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="ddbdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbdb-103">Lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="ddbdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddbdb-104">SYNTAX</span></span>

### <span data-ttu-id="ddbdb-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ddbdb-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddbdb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ddbdb-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddbdb-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddbdb-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddbdb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddbdb-108">DESCRIPTION</span></span>
<span data-ttu-id="ddbdb-109">A Get-AzNetworkWatcherReachabilityProvidersList lista todos os provedores de serviços de Internet disponíveis para uma região do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="ddbdb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddbdb-110">EXAMPLES</span></span>

### <span data-ttu-id="ddbdb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddbdb-111">Example 1</span></span>
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

<span data-ttu-id="ddbdb-112">Lista todos os provedores disponíveis em Seattle, WA para o Azure Data Center no oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="ddbdb-113">OS</span><span class="sxs-lookup"><span data-stu-id="ddbdb-113">PARAMETERS</span></span>

### <span data-ttu-id="ddbdb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddbdb-114">-AsJob</span></span>
<span data-ttu-id="ddbdb-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ddbdb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddbdb-116">-Cidade</span><span class="sxs-lookup"><span data-stu-id="ddbdb-116">-City</span></span>
<span data-ttu-id="ddbdb-117">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-117">The name of the city.</span></span>

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

### <span data-ttu-id="ddbdb-118">-País</span><span class="sxs-lookup"><span data-stu-id="ddbdb-118">-Country</span></span>
<span data-ttu-id="ddbdb-119">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-119">The name of the country.</span></span>

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

### <span data-ttu-id="ddbdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbdb-120">-DefaultProfile</span></span>
<span data-ttu-id="ddbdb-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddbdb-122">-Local</span><span class="sxs-lookup"><span data-stu-id="ddbdb-122">-Location</span></span>
<span data-ttu-id="ddbdb-123">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="ddbdb-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ddbdb-124">-NetworkWatcher</span></span>
<span data-ttu-id="ddbdb-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="ddbdb-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ddbdb-126">-NetworkWatcherName</span></span>
<span data-ttu-id="ddbdb-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="ddbdb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbdb-128">-ResourceGroupName</span></span>
<span data-ttu-id="ddbdb-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ddbdb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddbdb-130">-ResourceId</span></span>
<span data-ttu-id="ddbdb-131">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="ddbdb-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="ddbdb-132">-State</span></span>
<span data-ttu-id="ddbdb-133">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-133">The name of the state.</span></span>

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

### <span data-ttu-id="ddbdb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbdb-134">CommonParameters</span></span>
<span data-ttu-id="ddbdb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbdb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbdb-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbdb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbdb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddbdb-137">INPUTS</span></span>

### <span data-ttu-id="ddbdb-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ddbdb-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ddbdb-139">System. String System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ddbdb-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ddbdb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddbdb-140">OUTPUTS</span></span>

### <span data-ttu-id="ddbdb-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="ddbdb-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="ddbdb-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddbdb-142">NOTES</span></span>
<span data-ttu-id="ddbdb-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="ddbdb-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="ddbdb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddbdb-144">RELATED LINKS</span></span>

[<span data-ttu-id="ddbdb-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ddbdb-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ddbdb-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ddbdb-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ddbdb-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ddbdb-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ddbdb-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ddbdb-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ddbdb-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ddbdb-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ddbdb-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ddbdb-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ddbdb-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ddbdb-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ddbdb-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddbdb-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddbdb-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ddbdb-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ddbdb-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddbdb-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddbdb-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddbdb-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddbdb-156">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddbdb-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
