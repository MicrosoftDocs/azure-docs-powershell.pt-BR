---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428183"
---
# <span data-ttu-id="50eae-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="50eae-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="50eae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50eae-102">SYNOPSIS</span></span>
<span data-ttu-id="50eae-103">Obtém o resultado da solução de problemas da operação de solução de problemas executada anteriormente ou em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="50eae-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50eae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50eae-104">SYNTAX</span></span>

### <span data-ttu-id="50eae-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="50eae-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50eae-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="50eae-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50eae-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50eae-107">DESCRIPTION</span></span>
<span data-ttu-id="50eae-108">O cmdlet Get-AzureRmNetworkWatcherTroubleshootingResult Obtém o resultado da solução de problemas da operação Start-AzureRmNetworkWatcherResourceTroubleshooting executada anteriormente ou atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="50eae-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="50eae-109">Se a operação de solução de problemas estiver em andamento, esta operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="50eae-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="50eae-110">Atualmente, há suporte para gateways de rede virtual e conexões.</span><span class="sxs-lookup"><span data-stu-id="50eae-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="50eae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50eae-111">EXAMPLES</span></span>

### <span data-ttu-id="50eae-112">---Exemplo 1: iniciar a solução de problemas em um gateway de rede virtual e recuperar o resultado---</span><span class="sxs-lookup"><span data-stu-id="50eae-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="50eae-113">O exemplo acima começa a solução de problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="50eae-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="50eae-114">A operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="50eae-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="50eae-115">Após a solução de problemas ter começado, uma chamada de Get-AzureRmNetworkWatcherTroubleshootingResult é feita ao recurso para recuperar o resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="50eae-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="50eae-116">OS</span><span class="sxs-lookup"><span data-stu-id="50eae-116">PARAMETERS</span></span>

### <span data-ttu-id="50eae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50eae-117">-DefaultProfile</span></span>
<span data-ttu-id="50eae-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50eae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50eae-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50eae-119">-NetworkWatcher</span></span>
<span data-ttu-id="50eae-120">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="50eae-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="50eae-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="50eae-121">-NetworkWatcherName</span></span>
<span data-ttu-id="50eae-122">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="50eae-122">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50eae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50eae-123">-ResourceGroupName</span></span>
<span data-ttu-id="50eae-124">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="50eae-124">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50eae-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="50eae-125">-TargetResourceId</span></span>
<span data-ttu-id="50eae-126">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="50eae-126">The target resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50eae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50eae-127">CommonParameters</span></span>
<span data-ttu-id="50eae-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50eae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50eae-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50eae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50eae-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50eae-130">INPUTS</span></span>

### <span data-ttu-id="50eae-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50eae-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="50eae-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50eae-132">System.String</span></span>

## <span data-ttu-id="50eae-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50eae-133">OUTPUTS</span></span>

### <span data-ttu-id="50eae-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="50eae-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="50eae-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50eae-135">NOTES</span></span>
<span data-ttu-id="50eae-136">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, solução de problemas, VPN, conexão</span><span class="sxs-lookup"><span data-stu-id="50eae-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="50eae-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50eae-137">RELATED LINKS</span></span>

[<span data-ttu-id="50eae-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="50eae-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="50eae-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50eae-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="50eae-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50eae-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="50eae-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50eae-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="50eae-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50eae-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50eae-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="50eae-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="50eae-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50eae-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50eae-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50eae-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50eae-146">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50eae-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50eae-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="50eae-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="50eae-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="50eae-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="50eae-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="50eae-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="50eae-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="50eae-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)