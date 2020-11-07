---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776522"
---
# <span data-ttu-id="7aae9-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7aae9-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="7aae9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7aae9-102">SYNOPSIS</span></span>
<span data-ttu-id="7aae9-103">Configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="7aae9-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="7aae9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aae9-104">SYNTAX</span></span>

### <span data-ttu-id="7aae9-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7aae9-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aae9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7aae9-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7aae9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7aae9-107">DESCRIPTION</span></span>
<span data-ttu-id="7aae9-108">O Set-AzNetworkWatcherConfigFlowLog configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="7aae9-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="7aae9-109">As propriedades a serem configuradas incluem: se o recurso de log de fluxo está ou não habilitado para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="7aae9-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="7aae9-110">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7aae9-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="7aae9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7aae9-111">EXAMPLES</span></span>

### <span data-ttu-id="7aae9-112">---Exemplo 1: configurar o log de fluxo para um---de NSG especificado</span><span class="sxs-lookup"><span data-stu-id="7aae9-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="7aae9-113">Neste exemplo, configuramos o status do log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="7aae9-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="7aae9-114">Na resposta, vemos que o NSG especificado tem o log de fluxo habilitado e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="7aae9-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="7aae9-115">OS</span><span class="sxs-lookup"><span data-stu-id="7aae9-115">PARAMETERS</span></span>

### <span data-ttu-id="7aae9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7aae9-116">-AsJob</span></span>
<span data-ttu-id="7aae9-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7aae9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7aae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aae9-118">-DefaultProfile</span></span>
<span data-ttu-id="7aae9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7aae9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aae9-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="7aae9-120">-EnableFlowLog</span></span>
<span data-ttu-id="7aae9-121">Sinalizador para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7aae9-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aae9-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="7aae9-122">-EnableRetention</span></span>
<span data-ttu-id="7aae9-123">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="7aae9-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aae9-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7aae9-124">-NetworkWatcher</span></span>
<span data-ttu-id="7aae9-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7aae9-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="7aae9-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7aae9-126">-NetworkWatcherName</span></span>
<span data-ttu-id="7aae9-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7aae9-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="7aae9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aae9-128">-ResourceGroupName</span></span>
<span data-ttu-id="7aae9-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7aae9-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7aae9-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7aae9-130">-RetentionInDays</span></span>
<span data-ttu-id="7aae9-131">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7aae9-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aae9-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7aae9-132">-StorageAccountId</span></span>
<span data-ttu-id="7aae9-133">ID da conta de armazenamento que é usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7aae9-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="7aae9-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7aae9-134">-TargetResourceId</span></span>
<span data-ttu-id="7aae9-135">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="7aae9-135">The target resource ID.</span></span>

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

### <span data-ttu-id="7aae9-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7aae9-136">-Confirm</span></span>
<span data-ttu-id="7aae9-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aae9-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aae9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aae9-138">-WhatIf</span></span>
<span data-ttu-id="7aae9-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7aae9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7aae9-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7aae9-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aae9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aae9-141">CommonParameters</span></span>
<span data-ttu-id="7aae9-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aae9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aae9-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aae9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aae9-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7aae9-144">INPUTS</span></span>

### <span data-ttu-id="7aae9-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7aae9-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7aae9-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="7aae9-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="7aae9-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7aae9-147">OUTPUTS</span></span>

### <span data-ttu-id="7aae9-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="7aae9-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="7aae9-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7aae9-149">NOTES</span></span>
<span data-ttu-id="7aae9-150">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="7aae9-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="7aae9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7aae9-151">RELATED LINKS</span></span>

[<span data-ttu-id="7aae9-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7aae9-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7aae9-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7aae9-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7aae9-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7aae9-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7aae9-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7aae9-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7aae9-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7aae9-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7aae9-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7aae9-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7aae9-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7aae9-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7aae9-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7aae9-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7aae9-160">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7aae9-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7aae9-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7aae9-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7aae9-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7aae9-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7aae9-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7aae9-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7aae9-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7aae9-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7aae9-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7aae9-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7aae9-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7aae9-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
