---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: eb8997025a9fa73c394c2c51c23f00c211604cb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785307"
---
# <span data-ttu-id="a8730-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8730-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a8730-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8730-102">SYNOPSIS</span></span>
<span data-ttu-id="a8730-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="a8730-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8730-104">SYNTAX</span></span>

### <span data-ttu-id="a8730-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8730-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8730-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a8730-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8730-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8730-107">DESCRIPTION</span></span>
<span data-ttu-id="a8730-108">O Remove-AzureRmNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="a8730-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="a8730-109">É recomendável chamar Stop-AzureRmNetworkWatcherPacketCapture antes de chamar remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="a8730-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="a8730-110">Se a sessão de captura de pacotes estiver em execução quando Remove-AzureRmNetworkWatcherPacketCapture for chamado, a captura de pacotes pode não ser salva.</span><span class="sxs-lookup"><span data-stu-id="a8730-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="a8730-111">Se a sessão for interrompida antes da remoção, o arquivo. Cap contendo dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="a8730-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="a8730-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8730-112">EXAMPLES</span></span>

### <span data-ttu-id="a8730-113">---Exemplo 1: remover uma sessão de captura de pacote--</span><span class="sxs-lookup"><span data-stu-id="a8730-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a8730-114">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="a8730-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="a8730-115">OS</span><span class="sxs-lookup"><span data-stu-id="a8730-115">PARAMETERS</span></span>

### <span data-ttu-id="a8730-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8730-116">-AsJob</span></span>
<span data-ttu-id="a8730-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a8730-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8730-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8730-118">-DefaultProfile</span></span>
<span data-ttu-id="a8730-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8730-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8730-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8730-120">-NetworkWatcher</span></span>
<span data-ttu-id="a8730-121">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a8730-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a8730-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a8730-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a8730-123">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a8730-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="a8730-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a8730-124">-PacketCaptureName</span></span>
<span data-ttu-id="a8730-125">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="a8730-125">The packet capture name.</span></span>

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

### <span data-ttu-id="a8730-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8730-126">-PassThru</span></span>
<span data-ttu-id="a8730-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="a8730-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a8730-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8730-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8730-129">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="a8730-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a8730-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8730-130">-Confirm</span></span>
<span data-ttu-id="a8730-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8730-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8730-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8730-132">-WhatIf</span></span>
<span data-ttu-id="a8730-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8730-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8730-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8730-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8730-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8730-135">CommonParameters</span></span>
<span data-ttu-id="a8730-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8730-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8730-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8730-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8730-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8730-138">INPUTS</span></span>

### <span data-ttu-id="a8730-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8730-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a8730-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a8730-140">System.String</span></span>

## <span data-ttu-id="a8730-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8730-141">OUTPUTS</span></span>

### <span data-ttu-id="a8730-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8730-142">System.Object</span></span>

## <span data-ttu-id="a8730-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8730-143">NOTES</span></span>
<span data-ttu-id="a8730-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego, remover</span><span class="sxs-lookup"><span data-stu-id="a8730-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="a8730-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8730-145">RELATED LINKS</span></span>

[<span data-ttu-id="a8730-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8730-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8730-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a8730-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a8730-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8730-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8730-149">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8730-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8730-150">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8730-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8730-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8730-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8730-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8730-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8730-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a8730-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a8730-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a8730-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a8730-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a8730-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a8730-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a8730-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a8730-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a8730-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
