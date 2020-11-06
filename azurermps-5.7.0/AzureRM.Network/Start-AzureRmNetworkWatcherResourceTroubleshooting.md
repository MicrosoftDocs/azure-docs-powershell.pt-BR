---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 6c211bef936d6fa3077d066f7df190dbe6d4a47d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609508"
---
# <span data-ttu-id="84b8f-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84b8f-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="84b8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="84b8f-103">Inicia a solução de problemas em um recurso de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="84b8f-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84b8f-104">SYNTAX</span></span>

### <span data-ttu-id="84b8f-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="84b8f-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84b8f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="84b8f-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b8f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="84b8f-108">O cmdlet Start-AzureRmNetworkWatcherResourceTroubleshooting começa a solução de problemas para um recurso de rede no Azure e retorna informações sobre possíveis problemas e atenuações.</span><span class="sxs-lookup"><span data-stu-id="84b8f-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="84b8f-109">Atualmente, há suporte para gateways de rede virtual e conexões.</span><span class="sxs-lookup"><span data-stu-id="84b8f-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="84b8f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="84b8f-111">---Exemplo 1: iniciar a solução de problemas em um gateway de rede virtual---</span><span class="sxs-lookup"><span data-stu-id="84b8f-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="84b8f-112">O exemplo acima começa a solução de problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="84b8f-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="84b8f-113">A operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="84b8f-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="84b8f-114">OS</span><span class="sxs-lookup"><span data-stu-id="84b8f-114">PARAMETERS</span></span>

### <span data-ttu-id="84b8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b8f-115">-DefaultProfile</span></span>
<span data-ttu-id="84b8f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84b8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b8f-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b8f-117">-NetworkWatcher</span></span>
<span data-ttu-id="84b8f-118">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="84b8f-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="84b8f-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="84b8f-119">-NetworkWatcherName</span></span>
<span data-ttu-id="84b8f-120">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="84b8f-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="84b8f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b8f-121">-ResourceGroupName</span></span>
<span data-ttu-id="84b8f-122">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="84b8f-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="84b8f-123">-Storageid</span><span class="sxs-lookup"><span data-stu-id="84b8f-123">-StorageId</span></span>
<span data-ttu-id="84b8f-124">A ID de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84b8f-124">The storage ID.</span></span>

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

### <span data-ttu-id="84b8f-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="84b8f-125">-StoragePath</span></span>
<span data-ttu-id="84b8f-126">O caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84b8f-126">The storage path.</span></span>

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

### <span data-ttu-id="84b8f-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="84b8f-127">-TargetResourceId</span></span>
<span data-ttu-id="84b8f-128">Especifica a ID do recurso para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="84b8f-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="84b8f-129">Exemplo de formato: "/subscriptions/$ {SubscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="84b8f-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="84b8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b8f-130">CommonParameters</span></span>
<span data-ttu-id="84b8f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b8f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b8f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b8f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84b8f-133">INPUTS</span></span>

### <span data-ttu-id="84b8f-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b8f-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="84b8f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84b8f-135">System.String</span></span>

## <span data-ttu-id="84b8f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84b8f-136">OUTPUTS</span></span>

### <span data-ttu-id="84b8f-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="84b8f-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="84b8f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84b8f-138">NOTES</span></span>
<span data-ttu-id="84b8f-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, solução de problemas, VPN, conexão</span><span class="sxs-lookup"><span data-stu-id="84b8f-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="84b8f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84b8f-140">RELATED LINKS</span></span>

[<span data-ttu-id="84b8f-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="84b8f-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="84b8f-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b8f-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b8f-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b8f-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b8f-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b8f-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b8f-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b8f-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b8f-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84b8f-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="84b8f-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b8f-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b8f-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b8f-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b8f-149">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b8f-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b8f-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84b8f-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="84b8f-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84b8f-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="84b8f-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84b8f-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84b8f-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84b8f-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
