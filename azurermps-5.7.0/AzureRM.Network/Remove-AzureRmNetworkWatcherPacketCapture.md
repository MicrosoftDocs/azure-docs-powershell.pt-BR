---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440114"
---
# <span data-ttu-id="63e55-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63e55-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="63e55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63e55-102">SYNOPSIS</span></span>
<span data-ttu-id="63e55-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="63e55-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63e55-104">SYNTAX</span></span>

### <span data-ttu-id="63e55-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="63e55-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e55-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="63e55-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e55-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63e55-107">DESCRIPTION</span></span>
<span data-ttu-id="63e55-108">O Remove-AzureRmNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="63e55-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="63e55-109">É recomendável chamar Stop-AzureRmNetworkWatcherPacketCapture antes de chamar remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="63e55-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="63e55-110">Se a sessão de captura de pacotes estiver em execução quando Remove-AzureRmNetworkWatcherPacketCapture for chamado, a captura de pacotes pode não ser salva.</span><span class="sxs-lookup"><span data-stu-id="63e55-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="63e55-111">Se a sessão for interrompida antes da remoção, o arquivo. Cap contendo dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="63e55-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="63e55-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63e55-112">EXAMPLES</span></span>

### <span data-ttu-id="63e55-113">---Exemplo 1: remover uma sessão de captura de pacote--</span><span class="sxs-lookup"><span data-stu-id="63e55-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="63e55-114">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="63e55-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="63e55-115">OS</span><span class="sxs-lookup"><span data-stu-id="63e55-115">PARAMETERS</span></span>

### <span data-ttu-id="63e55-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63e55-116">-AsJob</span></span>
<span data-ttu-id="63e55-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="63e55-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63e55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e55-118">-DefaultProfile</span></span>
<span data-ttu-id="63e55-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63e55-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e55-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63e55-120">-NetworkWatcher</span></span>
<span data-ttu-id="63e55-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="63e55-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="63e55-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="63e55-122">-NetworkWatcherName</span></span>
<span data-ttu-id="63e55-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="63e55-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="63e55-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="63e55-124">-PacketCaptureName</span></span>
<span data-ttu-id="63e55-125">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="63e55-125">The packet capture name.</span></span>

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

### <span data-ttu-id="63e55-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63e55-126">-PassThru</span></span>
<span data-ttu-id="63e55-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="63e55-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e55-128">-ResourceGroupName</span></span>
<span data-ttu-id="63e55-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="63e55-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="63e55-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63e55-130">-Confirm</span></span>
<span data-ttu-id="63e55-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e55-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e55-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e55-132">-WhatIf</span></span>
<span data-ttu-id="63e55-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63e55-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e55-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63e55-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e55-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e55-135">CommonParameters</span></span>
<span data-ttu-id="63e55-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e55-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e55-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e55-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e55-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63e55-138">INPUTS</span></span>

### <span data-ttu-id="63e55-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63e55-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="63e55-140">System. String</span><span class="sxs-lookup"><span data-stu-id="63e55-140">System.String</span></span>

## <span data-ttu-id="63e55-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63e55-141">OUTPUTS</span></span>

### <span data-ttu-id="63e55-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="63e55-142">System.Object</span></span>

## <span data-ttu-id="63e55-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63e55-143">NOTES</span></span>
<span data-ttu-id="63e55-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego, remover</span><span class="sxs-lookup"><span data-stu-id="63e55-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="63e55-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e55-145">RELATED LINKS</span></span>

[<span data-ttu-id="63e55-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63e55-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63e55-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="63e55-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="63e55-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63e55-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63e55-149">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63e55-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63e55-150">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63e55-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="63e55-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63e55-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="63e55-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63e55-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="63e55-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="63e55-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="63e55-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="63e55-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="63e55-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="63e55-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="63e55-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="63e55-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="63e55-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="63e55-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
