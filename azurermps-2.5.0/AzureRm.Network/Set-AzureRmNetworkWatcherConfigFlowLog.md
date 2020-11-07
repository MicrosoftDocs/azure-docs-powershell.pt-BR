---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8e8462ded1f122a050c85877e8e82b2ecc0dd9d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785308"
---
# <span data-ttu-id="81ee6-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="81ee6-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="81ee6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="81ee6-103">Configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="81ee6-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ee6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81ee6-104">SYNTAX</span></span>

### <span data-ttu-id="81ee6-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="81ee6-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81ee6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="81ee6-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81ee6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="81ee6-108">O Set-AzureRmNetworkWatcherConfigFlowLog configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="81ee6-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="81ee6-109">As propriedades a serem configuradas incluem: se o recurso de log de fluxo está ou não habilitado para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="81ee6-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="81ee6-110">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="81ee6-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="81ee6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81ee6-111">EXAMPLES</span></span>

### <span data-ttu-id="81ee6-112">---Exemplo 1: configurar o log de fluxo para um---de NSG especificado</span><span class="sxs-lookup"><span data-stu-id="81ee6-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="81ee6-113">Neste exemplo, configuramos o status do log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="81ee6-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="81ee6-114">Na resposta, vemos que o NSG especificado tem o log de fluxo habilitado e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="81ee6-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="81ee6-115">OS</span><span class="sxs-lookup"><span data-stu-id="81ee6-115">PARAMETERS</span></span>

### <span data-ttu-id="81ee6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81ee6-116">-AsJob</span></span>
<span data-ttu-id="81ee6-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="81ee6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81ee6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ee6-118">-DefaultProfile</span></span>
<span data-ttu-id="81ee6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81ee6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81ee6-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="81ee6-120">-EnableFlowLog</span></span>
<span data-ttu-id="81ee6-121">Sinalizador para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="81ee6-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="81ee6-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="81ee6-122">-EnableRetention</span></span>
<span data-ttu-id="81ee6-123">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="81ee6-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="81ee6-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81ee6-124">-NetworkWatcher</span></span>
<span data-ttu-id="81ee6-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="81ee6-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="81ee6-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="81ee6-126">-NetworkWatcherName</span></span>
<span data-ttu-id="81ee6-127">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="81ee6-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="81ee6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ee6-128">-ResourceGroupName</span></span>
<span data-ttu-id="81ee6-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="81ee6-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="81ee6-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="81ee6-130">-RetentionInDays</span></span>
<span data-ttu-id="81ee6-131">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="81ee6-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="81ee6-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="81ee6-132">-StorageAccountId</span></span>
<span data-ttu-id="81ee6-133">ID da conta de armazenamento que é usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="81ee6-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="81ee6-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="81ee6-134">-TargetResourceId</span></span>
<span data-ttu-id="81ee6-135">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="81ee6-135">The target resource ID.</span></span>

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

### <span data-ttu-id="81ee6-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81ee6-136">-Confirm</span></span>
<span data-ttu-id="81ee6-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ee6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81ee6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ee6-138">-WhatIf</span></span>
<span data-ttu-id="81ee6-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81ee6-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81ee6-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81ee6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81ee6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ee6-141">CommonParameters</span></span>
<span data-ttu-id="81ee6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ee6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ee6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ee6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ee6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81ee6-144">INPUTS</span></span>

### <span data-ttu-id="81ee6-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81ee6-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="81ee6-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="81ee6-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="81ee6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81ee6-147">OUTPUTS</span></span>

### <span data-ttu-id="81ee6-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="81ee6-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="81ee6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81ee6-149">NOTES</span></span>
<span data-ttu-id="81ee6-150">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="81ee6-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="81ee6-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81ee6-151">RELATED LINKS</span></span>

[<span data-ttu-id="81ee6-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="81ee6-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="81ee6-153">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81ee6-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="81ee6-154">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81ee6-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="81ee6-155">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81ee6-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="81ee6-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81ee6-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81ee6-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="81ee6-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="81ee6-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81ee6-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81ee6-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81ee6-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81ee6-160">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="81ee6-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="81ee6-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="81ee6-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="81ee6-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="81ee6-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="81ee6-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="81ee6-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="81ee6-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="81ee6-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="81ee6-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="81ee6-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="81ee6-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="81ee6-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
