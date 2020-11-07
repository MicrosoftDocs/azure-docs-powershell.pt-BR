---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786454"
---
# <span data-ttu-id="43a04-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43a04-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="43a04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43a04-102">SYNOPSIS</span></span>
<span data-ttu-id="43a04-103">Obtém as propriedades de um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="43a04-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43a04-104">SYNTAX</span></span>

### <span data-ttu-id="43a04-105">Obter</span><span class="sxs-lookup"><span data-stu-id="43a04-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43a04-106">Programação</span><span class="sxs-lookup"><span data-stu-id="43a04-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43a04-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43a04-107">DESCRIPTION</span></span>
<span data-ttu-id="43a04-108">O cmdlet Get-AzureRmNetworkWatcher Obtém um ou mais recursos do Inspetor de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="43a04-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="43a04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43a04-109">EXAMPLES</span></span>

### <span data-ttu-id="43a04-110">--------------------------Exemplo 1: obter um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="43a04-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="43a04-111">Obtém o Inspetor de rede chamado NetworkWatcher_westcentralus na NetworkWatcherRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43a04-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="43a04-112">OS</span><span class="sxs-lookup"><span data-stu-id="43a04-112">PARAMETERS</span></span>

### <span data-ttu-id="43a04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a04-113">-DefaultProfile</span></span>
<span data-ttu-id="43a04-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43a04-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a04-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="43a04-115">-Name</span></span>
<span data-ttu-id="43a04-116">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="43a04-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a04-117">-ResourceGroupName</span></span>
<span data-ttu-id="43a04-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43a04-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43a04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a04-119">CommonParameters</span></span>
<span data-ttu-id="43a04-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a04-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a04-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43a04-122">INPUTS</span></span>

### <span data-ttu-id="43a04-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="43a04-123">None</span></span>

## <span data-ttu-id="43a04-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43a04-124">OUTPUTS</span></span>

### <span data-ttu-id="43a04-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43a04-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="43a04-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43a04-126">NOTES</span></span>
<span data-ttu-id="43a04-127">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="43a04-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="43a04-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43a04-128">RELATED LINKS</span></span>

[<span data-ttu-id="43a04-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43a04-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="43a04-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43a04-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="43a04-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43a04-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43a04-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="43a04-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="43a04-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43a04-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43a04-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43a04-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43a04-135">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43a04-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43a04-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="43a04-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="43a04-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="43a04-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="43a04-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="43a04-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="43a04-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="43a04-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="43a04-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="43a04-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
