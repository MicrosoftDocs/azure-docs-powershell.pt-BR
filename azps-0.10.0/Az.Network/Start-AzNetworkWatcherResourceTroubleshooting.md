---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776486"
---
# <span data-ttu-id="adad6-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="adad6-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="adad6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adad6-102">SYNOPSIS</span></span>
<span data-ttu-id="adad6-103">Inicia a solução de problemas em um recurso de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="adad6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="adad6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adad6-104">SYNTAX</span></span>

### <span data-ttu-id="adad6-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="adad6-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adad6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="adad6-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adad6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adad6-107">DESCRIPTION</span></span>
<span data-ttu-id="adad6-108">O cmdlet Start-AzNetworkWatcherResourceTroubleshooting começa a solução de problemas para um recurso de rede no Azure e retorna informações sobre possíveis problemas e atenuações.</span><span class="sxs-lookup"><span data-stu-id="adad6-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="adad6-109">Atualmente, há suporte para gateways de rede virtual e conexões.</span><span class="sxs-lookup"><span data-stu-id="adad6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="adad6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adad6-110">EXAMPLES</span></span>

### <span data-ttu-id="adad6-111">---Exemplo 1: iniciar a solução de problemas em um gateway de rede virtual---</span><span class="sxs-lookup"><span data-stu-id="adad6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="adad6-112">O exemplo acima começa a solução de problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="adad6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="adad6-113">A operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="adad6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="adad6-114">OS</span><span class="sxs-lookup"><span data-stu-id="adad6-114">PARAMETERS</span></span>

### <span data-ttu-id="adad6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adad6-115">-DefaultProfile</span></span>
<span data-ttu-id="adad6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adad6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adad6-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adad6-117">-NetworkWatcher</span></span>
<span data-ttu-id="adad6-118">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="adad6-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="adad6-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="adad6-119">-NetworkWatcherName</span></span>
<span data-ttu-id="adad6-120">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="adad6-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="adad6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adad6-121">-ResourceGroupName</span></span>
<span data-ttu-id="adad6-122">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="adad6-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="adad6-123">-Storageid</span><span class="sxs-lookup"><span data-stu-id="adad6-123">-StorageId</span></span>
<span data-ttu-id="adad6-124">A ID de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="adad6-124">The storage ID.</span></span>

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

### <span data-ttu-id="adad6-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="adad6-125">-StoragePath</span></span>
<span data-ttu-id="adad6-126">O caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="adad6-126">The storage path.</span></span>

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

### <span data-ttu-id="adad6-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="adad6-127">-TargetResourceId</span></span>
<span data-ttu-id="adad6-128">Especifica a ID do recurso para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="adad6-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="adad6-129">Exemplo de formato: "/subscriptions/$ {SubscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="adad6-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="adad6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adad6-130">CommonParameters</span></span>
<span data-ttu-id="adad6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adad6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adad6-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adad6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adad6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adad6-133">INPUTS</span></span>

### <span data-ttu-id="adad6-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adad6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="adad6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="adad6-135">System.String</span></span>

## <span data-ttu-id="adad6-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adad6-136">OUTPUTS</span></span>

### <span data-ttu-id="adad6-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="adad6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="adad6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adad6-138">NOTES</span></span>
<span data-ttu-id="adad6-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, solução de problemas, VPN, conexão</span><span class="sxs-lookup"><span data-stu-id="adad6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="adad6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adad6-140">RELATED LINKS</span></span>

[<span data-ttu-id="adad6-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="adad6-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="adad6-142">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adad6-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="adad6-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adad6-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="adad6-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adad6-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="adad6-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adad6-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adad6-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="adad6-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="adad6-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adad6-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adad6-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adad6-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adad6-149">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adad6-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adad6-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="adad6-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="adad6-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="adad6-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="adad6-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="adad6-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="adad6-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="adad6-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
