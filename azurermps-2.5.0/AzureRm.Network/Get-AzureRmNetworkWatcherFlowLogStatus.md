---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785495"
---
# <span data-ttu-id="b70db-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b70db-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="b70db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b70db-102">SYNOPSIS</span></span>
<span data-ttu-id="b70db-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="b70db-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b70db-104">SYNTAX</span></span>

### <span data-ttu-id="b70db-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b70db-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b70db-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b70db-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b70db-107">DESCRIPTION</span></span>
<span data-ttu-id="b70db-108">O cmdlet Get-AzureRmNetworkWatcherFlowLogStatus Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="b70db-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="b70db-109">O status inclui se o registro em log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="b70db-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="b70db-110">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b70db-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="b70db-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b70db-111">EXAMPLES</span></span>

### <span data-ttu-id="b70db-112">---Exemplo 1: obter o status de log de fluxo de um NSG especificado---</span><span class="sxs-lookup"><span data-stu-id="b70db-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="b70db-113">Neste exemplo, obtemos o status de log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b70db-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="b70db-114">O NSG especificado tem o log de fluxo habilitado e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="b70db-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="b70db-115">OS</span><span class="sxs-lookup"><span data-stu-id="b70db-115">PARAMETERS</span></span>

### <span data-ttu-id="b70db-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b70db-116">-AsJob</span></span>
<span data-ttu-id="b70db-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b70db-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b70db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70db-118">-DefaultProfile</span></span>
<span data-ttu-id="b70db-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b70db-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70db-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70db-120">-NetworkWatcher</span></span>
<span data-ttu-id="b70db-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b70db-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="b70db-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b70db-122">-NetworkWatcherName</span></span>
<span data-ttu-id="b70db-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b70db-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="b70db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70db-124">-ResourceGroupName</span></span>
<span data-ttu-id="b70db-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b70db-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b70db-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b70db-126">-TargetResourceId</span></span>
<span data-ttu-id="b70db-127">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="b70db-127">The target resource ID.</span></span>

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

### <span data-ttu-id="b70db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70db-128">CommonParameters</span></span>
<span data-ttu-id="b70db-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70db-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70db-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b70db-131">INPUTS</span></span>

### <span data-ttu-id="b70db-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70db-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b70db-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b70db-133">System.String</span></span>

## <span data-ttu-id="b70db-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b70db-134">OUTPUTS</span></span>

### <span data-ttu-id="b70db-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="b70db-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="b70db-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b70db-136">NOTES</span></span>
<span data-ttu-id="b70db-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="b70db-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="b70db-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b70db-138">RELATED LINKS</span></span>

[<span data-ttu-id="b70db-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b70db-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b70db-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70db-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b70db-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70db-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b70db-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70db-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b70db-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70db-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70db-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b70db-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b70db-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70db-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70db-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70db-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70db-147">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70db-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70db-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b70db-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b70db-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b70db-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b70db-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b70db-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b70db-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b70db-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b70db-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b70db-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b70db-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b70db-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
