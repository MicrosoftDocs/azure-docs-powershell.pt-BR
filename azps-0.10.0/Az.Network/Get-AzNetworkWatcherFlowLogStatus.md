---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775507"
---
# <span data-ttu-id="24f0c-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="24f0c-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="24f0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="24f0c-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="24f0c-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="24f0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24f0c-104">SYNTAX</span></span>

### <span data-ttu-id="24f0c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="24f0c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f0c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="24f0c-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24f0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24f0c-107">DESCRIPTION</span></span>
<span data-ttu-id="24f0c-108">O cmdlet Get-AzNetworkWatcherFlowLogStatus Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="24f0c-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="24f0c-109">O status inclui se o registro em log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="24f0c-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="24f0c-110">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="24f0c-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="24f0c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24f0c-111">EXAMPLES</span></span>

### <span data-ttu-id="24f0c-112">---Exemplo 1: obter o status de log de fluxo de um NSG especificado---</span><span class="sxs-lookup"><span data-stu-id="24f0c-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="24f0c-113">Neste exemplo, obtemos o status de log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="24f0c-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="24f0c-114">O NSG especificado tem o log de fluxo habilitado e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="24f0c-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="24f0c-115">OS</span><span class="sxs-lookup"><span data-stu-id="24f0c-115">PARAMETERS</span></span>

### <span data-ttu-id="24f0c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f0c-116">-AsJob</span></span>
<span data-ttu-id="24f0c-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="24f0c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f0c-118">-DefaultProfile</span></span>
<span data-ttu-id="24f0c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24f0c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f0c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f0c-120">-NetworkWatcher</span></span>
<span data-ttu-id="24f0c-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="24f0c-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="24f0c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="24f0c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="24f0c-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="24f0c-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="24f0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="24f0c-125">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="24f0c-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="24f0c-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="24f0c-126">-TargetResourceId</span></span>
<span data-ttu-id="24f0c-127">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="24f0c-127">The target resource ID.</span></span>

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

### <span data-ttu-id="24f0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f0c-128">CommonParameters</span></span>
<span data-ttu-id="24f0c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f0c-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f0c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f0c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24f0c-131">INPUTS</span></span>

### <span data-ttu-id="24f0c-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f0c-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="24f0c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="24f0c-133">System.String</span></span>

## <span data-ttu-id="24f0c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24f0c-134">OUTPUTS</span></span>

### <span data-ttu-id="24f0c-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="24f0c-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="24f0c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24f0c-136">NOTES</span></span>
<span data-ttu-id="24f0c-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="24f0c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="24f0c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24f0c-138">RELATED LINKS</span></span>

[<span data-ttu-id="24f0c-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="24f0c-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="24f0c-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f0c-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="24f0c-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f0c-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="24f0c-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f0c-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="24f0c-143">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f0c-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f0c-144">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="24f0c-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="24f0c-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f0c-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f0c-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f0c-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f0c-147">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f0c-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f0c-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="24f0c-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="24f0c-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="24f0c-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="24f0c-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="24f0c-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="24f0c-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="24f0c-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="24f0c-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="24f0c-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="24f0c-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="24f0c-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
