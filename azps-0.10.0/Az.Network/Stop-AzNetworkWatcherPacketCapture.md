---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776480"
---
# <span data-ttu-id="58334-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58334-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="58334-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58334-102">SYNOPSIS</span></span>
<span data-ttu-id="58334-103">Interrompe uma sessão de captura de pacote em execução</span><span class="sxs-lookup"><span data-stu-id="58334-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="58334-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58334-104">SYNTAX</span></span>

### <span data-ttu-id="58334-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="58334-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58334-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="58334-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58334-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58334-107">DESCRIPTION</span></span>
<span data-ttu-id="58334-108">O Stop-AzNetworkWatcherPacketCapture para de uma sessão de captura de pacote em execução.</span><span class="sxs-lookup"><span data-stu-id="58334-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="58334-109">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="58334-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="58334-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58334-110">EXAMPLES</span></span>

### <span data-ttu-id="58334-111">---Exemplo 1: parar uma sessão de captura de pacote---</span><span class="sxs-lookup"><span data-stu-id="58334-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="58334-112">Neste exemplo, vamos parar uma sessão de captura de pacote em execução chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="58334-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="58334-113">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="58334-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="58334-114">OS</span><span class="sxs-lookup"><span data-stu-id="58334-114">PARAMETERS</span></span>

### <span data-ttu-id="58334-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58334-115">-AsJob</span></span>
<span data-ttu-id="58334-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="58334-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58334-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58334-117">-DefaultProfile</span></span>
<span data-ttu-id="58334-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58334-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58334-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58334-119">-NetworkWatcher</span></span>
<span data-ttu-id="58334-120">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="58334-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="58334-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="58334-121">-NetworkWatcherName</span></span>
<span data-ttu-id="58334-122">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="58334-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="58334-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="58334-123">-PacketCaptureName</span></span>
<span data-ttu-id="58334-124">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="58334-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58334-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58334-125">-PassThru</span></span>
<span data-ttu-id="58334-126">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="58334-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="58334-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58334-127">-ResourceGroupName</span></span>
<span data-ttu-id="58334-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="58334-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="58334-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58334-129">-Confirm</span></span>
<span data-ttu-id="58334-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58334-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58334-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58334-131">-WhatIf</span></span>
<span data-ttu-id="58334-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58334-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58334-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58334-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58334-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58334-134">CommonParameters</span></span>
<span data-ttu-id="58334-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58334-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58334-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58334-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58334-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58334-137">INPUTS</span></span>

### <span data-ttu-id="58334-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58334-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="58334-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58334-139">System.String</span></span>

## <span data-ttu-id="58334-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58334-140">OUTPUTS</span></span>

### <span data-ttu-id="58334-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58334-141">System.Boolean</span></span>

## <span data-ttu-id="58334-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58334-142">NOTES</span></span>
<span data-ttu-id="58334-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="58334-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="58334-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58334-144">RELATED LINKS</span></span>

[<span data-ttu-id="58334-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58334-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58334-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="58334-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="58334-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58334-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58334-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58334-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58334-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58334-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="58334-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58334-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="58334-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58334-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="58334-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="58334-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="58334-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="58334-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="58334-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="58334-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="58334-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="58334-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="58334-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="58334-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
