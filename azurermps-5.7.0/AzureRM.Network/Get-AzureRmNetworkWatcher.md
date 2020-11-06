---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: 9df0d0855ca22e9ea7141a99c69c8b44f16f489d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441312"
---
# <span data-ttu-id="0d5eb-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d5eb-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="0d5eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5eb-103">Obtém as propriedades de um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="0d5eb-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d5eb-104">SYNTAX</span></span>

### <span data-ttu-id="0d5eb-105">Obter</span><span class="sxs-lookup"><span data-stu-id="0d5eb-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d5eb-106">Programação</span><span class="sxs-lookup"><span data-stu-id="0d5eb-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d5eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d5eb-107">DESCRIPTION</span></span>
<span data-ttu-id="0d5eb-108">O cmdlet Get-AzureRmNetworkWatcher Obtém um ou mais recursos do Inspetor de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="0d5eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d5eb-109">EXAMPLES</span></span>

### <span data-ttu-id="0d5eb-110">--------------------------Exemplo 1: obter um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d5eb-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="0d5eb-111">Obtém o Inspetor de rede chamado NetworkWatcher_westcentralus na NetworkWatcherRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="0d5eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d5eb-112">PARAMETERS</span></span>

### <span data-ttu-id="0d5eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5eb-113">-DefaultProfile</span></span>
<span data-ttu-id="0d5eb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5eb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d5eb-115">-Name</span></span>
<span data-ttu-id="0d5eb-116">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-116">The network watcher name.</span></span>

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

### <span data-ttu-id="0d5eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d5eb-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-118">The resource group name.</span></span>

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

### <span data-ttu-id="0d5eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5eb-119">CommonParameters</span></span>
<span data-ttu-id="0d5eb-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5eb-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5eb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5eb-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d5eb-122">INPUTS</span></span>

### <span data-ttu-id="0d5eb-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0d5eb-123">None</span></span>

## <span data-ttu-id="0d5eb-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d5eb-124">OUTPUTS</span></span>

### <span data-ttu-id="0d5eb-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d5eb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0d5eb-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d5eb-126">NOTES</span></span>
<span data-ttu-id="0d5eb-127">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="0d5eb-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="0d5eb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d5eb-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d5eb-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d5eb-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d5eb-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d5eb-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d5eb-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d5eb-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d5eb-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0d5eb-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0d5eb-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d5eb-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d5eb-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d5eb-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d5eb-135">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d5eb-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d5eb-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d5eb-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0d5eb-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d5eb-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0d5eb-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0d5eb-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0d5eb-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0d5eb-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0d5eb-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0d5eb-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
