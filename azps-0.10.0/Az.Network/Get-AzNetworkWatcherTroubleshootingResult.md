---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775500"
---
# <span data-ttu-id="0dc07-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0dc07-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="0dc07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dc07-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc07-103">Obtém o resultado da solução de problemas da operação de solução de problemas executada anteriormente ou em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0dc07-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="0dc07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc07-104">SYNTAX</span></span>

### <span data-ttu-id="0dc07-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dc07-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc07-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0dc07-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dc07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dc07-107">DESCRIPTION</span></span>
<span data-ttu-id="0dc07-108">O cmdlet Get-AzNetworkWatcherTroubleshootingResult Obtém o resultado da solução de problemas da operação Start-AzNetworkWatcherResourceTroubleshooting executada anteriormente ou atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="0dc07-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="0dc07-109">Se a operação de solução de problemas estiver em andamento, esta operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="0dc07-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="0dc07-110">Atualmente, há suporte para gateways de rede virtual e conexões.</span><span class="sxs-lookup"><span data-stu-id="0dc07-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="0dc07-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dc07-111">EXAMPLES</span></span>

### <span data-ttu-id="0dc07-112">---Exemplo 1: iniciar a solução de problemas em um gateway de rede virtual e recuperar o resultado---</span><span class="sxs-lookup"><span data-stu-id="0dc07-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="0dc07-113">O exemplo acima começa a solução de problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0dc07-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="0dc07-114">A operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="0dc07-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="0dc07-115">Após a solução de problemas ter começado, uma chamada de Get-AzNetworkWatcherTroubleshootingResult é feita ao recurso para recuperar o resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="0dc07-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="0dc07-116">OS</span><span class="sxs-lookup"><span data-stu-id="0dc07-116">PARAMETERS</span></span>

### <span data-ttu-id="0dc07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc07-117">-DefaultProfile</span></span>
<span data-ttu-id="0dc07-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc07-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dc07-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dc07-119">-NetworkWatcher</span></span>
<span data-ttu-id="0dc07-120">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="0dc07-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="0dc07-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0dc07-121">-NetworkWatcherName</span></span>
<span data-ttu-id="0dc07-122">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="0dc07-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="0dc07-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc07-123">-ResourceGroupName</span></span>
<span data-ttu-id="0dc07-124">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="0dc07-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0dc07-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0dc07-125">-TargetResourceId</span></span>
<span data-ttu-id="0dc07-126">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="0dc07-126">The target resource ID.</span></span>

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

### <span data-ttu-id="0dc07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc07-127">CommonParameters</span></span>
<span data-ttu-id="0dc07-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc07-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc07-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc07-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dc07-130">INPUTS</span></span>

### <span data-ttu-id="0dc07-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dc07-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0dc07-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc07-132">System.String</span></span>

## <span data-ttu-id="0dc07-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dc07-133">OUTPUTS</span></span>

### <span data-ttu-id="0dc07-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="0dc07-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="0dc07-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dc07-135">NOTES</span></span>
<span data-ttu-id="0dc07-136">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, solução de problemas, VPN, conexão</span><span class="sxs-lookup"><span data-stu-id="0dc07-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="0dc07-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dc07-137">RELATED LINKS</span></span>

[<span data-ttu-id="0dc07-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0dc07-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0dc07-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dc07-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0dc07-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dc07-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0dc07-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dc07-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0dc07-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dc07-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dc07-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0dc07-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0dc07-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dc07-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dc07-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dc07-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dc07-146">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dc07-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dc07-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0dc07-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0dc07-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0dc07-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0dc07-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0dc07-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0dc07-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0dc07-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
