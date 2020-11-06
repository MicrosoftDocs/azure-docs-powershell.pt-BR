---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1904e9df565a5f9e8d3738e723348ec96010f97a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430981"
---
# <span data-ttu-id="1fa53-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1fa53-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="1fa53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fa53-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa53-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="1fa53-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fa53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fa53-104">SYNTAX</span></span>

### <span data-ttu-id="1fa53-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fa53-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fa53-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1fa53-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa53-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fa53-107">DESCRIPTION</span></span>
<span data-ttu-id="1fa53-108">O cmdlet Get-AzureRmNetworkWatcherFlowLogStatus Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="1fa53-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="1fa53-109">O status inclui se o registro em log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="1fa53-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="1fa53-110">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1fa53-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="1fa53-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fa53-111">EXAMPLES</span></span>

### <span data-ttu-id="1fa53-112">---Exemplo 1: obter o status de log de fluxo de um NSG especificado---</span><span class="sxs-lookup"><span data-stu-id="1fa53-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="1fa53-113">Neste exemplo, obtemos o status de log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1fa53-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="1fa53-114">O NSG especificado tem o log de fluxo habilitado e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="1fa53-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="1fa53-115">OS</span><span class="sxs-lookup"><span data-stu-id="1fa53-115">PARAMETERS</span></span>

### <span data-ttu-id="1fa53-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fa53-116">-AsJob</span></span>
<span data-ttu-id="1fa53-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1fa53-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fa53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa53-118">-DefaultProfile</span></span>
<span data-ttu-id="1fa53-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa53-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa53-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1fa53-120">-NetworkWatcher</span></span>
<span data-ttu-id="1fa53-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1fa53-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="1fa53-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1fa53-122">-NetworkWatcherName</span></span>
<span data-ttu-id="1fa53-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1fa53-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="1fa53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa53-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fa53-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1fa53-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1fa53-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa53-126">-TargetResourceId</span></span>
<span data-ttu-id="1fa53-127">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="1fa53-127">The target resource ID.</span></span>

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

### <span data-ttu-id="1fa53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa53-128">CommonParameters</span></span>
<span data-ttu-id="1fa53-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa53-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa53-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa53-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fa53-131">INPUTS</span></span>

### <span data-ttu-id="1fa53-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1fa53-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1fa53-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1fa53-133">System.String</span></span>

## <span data-ttu-id="1fa53-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fa53-134">OUTPUTS</span></span>

### <span data-ttu-id="1fa53-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="1fa53-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="1fa53-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fa53-136">NOTES</span></span>
<span data-ttu-id="1fa53-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="1fa53-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="1fa53-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fa53-138">RELATED LINKS</span></span>

[<span data-ttu-id="1fa53-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1fa53-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1fa53-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1fa53-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1fa53-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1fa53-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1fa53-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1fa53-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1fa53-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1fa53-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1fa53-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1fa53-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1fa53-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1fa53-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1fa53-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1fa53-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1fa53-147">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1fa53-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1fa53-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1fa53-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1fa53-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1fa53-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1fa53-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1fa53-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1fa53-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1fa53-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1fa53-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1fa53-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1fa53-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1fa53-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
