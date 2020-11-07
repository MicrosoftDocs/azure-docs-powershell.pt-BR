---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776619"
---
# <span data-ttu-id="885ab-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="885ab-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="885ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="885ab-102">SYNOPSIS</span></span>
<span data-ttu-id="885ab-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="885ab-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="885ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="885ab-104">SYNTAX</span></span>

### <span data-ttu-id="885ab-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="885ab-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885ab-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="885ab-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885ab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="885ab-107">DESCRIPTION</span></span>
<span data-ttu-id="885ab-108">O Remove-AzNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="885ab-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="885ab-109">É recomendável chamar Stop-AzNetworkWatcherPacketCapture antes de chamar remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="885ab-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="885ab-110">Se a sessão de captura de pacotes estiver em execução quando Remove-AzNetworkWatcherPacketCapture for chamado, a captura de pacotes pode não ser salva.</span><span class="sxs-lookup"><span data-stu-id="885ab-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="885ab-111">Se a sessão for interrompida antes da remoção, o arquivo. Cap contendo dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="885ab-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="885ab-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="885ab-112">EXAMPLES</span></span>

### <span data-ttu-id="885ab-113">---Exemplo 1: remover uma sessão de captura de pacote--</span><span class="sxs-lookup"><span data-stu-id="885ab-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="885ab-114">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="885ab-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="885ab-115">OS</span><span class="sxs-lookup"><span data-stu-id="885ab-115">PARAMETERS</span></span>

### <span data-ttu-id="885ab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="885ab-116">-AsJob</span></span>
<span data-ttu-id="885ab-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="885ab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="885ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885ab-118">-DefaultProfile</span></span>
<span data-ttu-id="885ab-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="885ab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="885ab-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="885ab-120">-NetworkWatcher</span></span>
<span data-ttu-id="885ab-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="885ab-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="885ab-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="885ab-122">-NetworkWatcherName</span></span>
<span data-ttu-id="885ab-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="885ab-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="885ab-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="885ab-124">-PacketCaptureName</span></span>
<span data-ttu-id="885ab-125">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="885ab-125">The packet capture name.</span></span>

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

### <span data-ttu-id="885ab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="885ab-126">-PassThru</span></span>
<span data-ttu-id="885ab-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="885ab-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="885ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="885ab-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="885ab-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="885ab-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="885ab-130">-Confirm</span></span>
<span data-ttu-id="885ab-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="885ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885ab-132">-WhatIf</span></span>
<span data-ttu-id="885ab-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="885ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885ab-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="885ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885ab-135">CommonParameters</span></span>
<span data-ttu-id="885ab-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885ab-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885ab-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885ab-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="885ab-138">INPUTS</span></span>

### <span data-ttu-id="885ab-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="885ab-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="885ab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="885ab-140">System.String</span></span>

## <span data-ttu-id="885ab-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="885ab-141">OUTPUTS</span></span>

### <span data-ttu-id="885ab-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="885ab-142">System.Object</span></span>

## <span data-ttu-id="885ab-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="885ab-143">NOTES</span></span>
<span data-ttu-id="885ab-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego, remover</span><span class="sxs-lookup"><span data-stu-id="885ab-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="885ab-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="885ab-145">RELATED LINKS</span></span>

[<span data-ttu-id="885ab-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="885ab-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="885ab-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="885ab-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="885ab-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="885ab-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="885ab-149">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="885ab-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="885ab-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="885ab-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="885ab-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="885ab-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="885ab-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="885ab-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="885ab-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="885ab-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="885ab-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="885ab-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="885ab-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="885ab-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="885ab-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="885ab-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="885ab-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="885ab-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)