---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775519"
---
# <span data-ttu-id="d7017-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7017-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="d7017-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7017-102">SYNOPSIS</span></span>
<span data-ttu-id="d7017-103">Obtém as propriedades de um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="d7017-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="d7017-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7017-104">SYNTAX</span></span>

### <span data-ttu-id="d7017-105">Obter</span><span class="sxs-lookup"><span data-stu-id="d7017-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7017-106">Programação</span><span class="sxs-lookup"><span data-stu-id="d7017-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7017-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7017-107">DESCRIPTION</span></span>
<span data-ttu-id="d7017-108">O cmdlet Get-AzNetworkWatcher Obtém um ou mais recursos do Inspetor de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7017-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="d7017-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7017-109">EXAMPLES</span></span>

### <span data-ttu-id="d7017-110">--------------------------Exemplo 1: obter um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="d7017-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="d7017-111">Obtém o Inspetor de rede chamado NetworkWatcher_westcentralus na NetworkWatcherRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7017-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="d7017-112">OS</span><span class="sxs-lookup"><span data-stu-id="d7017-112">PARAMETERS</span></span>

### <span data-ttu-id="d7017-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7017-113">-DefaultProfile</span></span>
<span data-ttu-id="d7017-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7017-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7017-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7017-115">-Name</span></span>
<span data-ttu-id="d7017-116">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="d7017-116">The network watcher name.</span></span>

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

### <span data-ttu-id="d7017-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7017-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7017-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7017-118">The resource group name.</span></span>

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

### <span data-ttu-id="d7017-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7017-119">CommonParameters</span></span>
<span data-ttu-id="d7017-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7017-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7017-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7017-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7017-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7017-122">INPUTS</span></span>

### <span data-ttu-id="d7017-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7017-123">None</span></span>

## <span data-ttu-id="d7017-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7017-124">OUTPUTS</span></span>

### <span data-ttu-id="d7017-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7017-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d7017-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7017-126">NOTES</span></span>
<span data-ttu-id="d7017-127">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="d7017-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="d7017-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7017-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7017-129">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7017-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d7017-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7017-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d7017-131">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7017-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7017-132">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7017-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d7017-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7017-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7017-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7017-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7017-135">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7017-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7017-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7017-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d7017-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7017-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d7017-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7017-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d7017-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7017-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d7017-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7017-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
