---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610359"
---
# <span data-ttu-id="d9fb4-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9fb4-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d9fb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fb4-103">Interrompe uma sessão de captura de pacote em execução</span><span class="sxs-lookup"><span data-stu-id="d9fb4-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9fb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9fb4-104">SYNTAX</span></span>

### <span data-ttu-id="d9fb4-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9fb4-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fb4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d9fb4-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9fb4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="d9fb4-108">O Stop-AzureRmNetworkWatcherPacketCapture para de uma sessão de captura de pacote em execução.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="d9fb4-109">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d9fb4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="d9fb4-111">---Exemplo 1: parar uma sessão de captura de pacote---</span><span class="sxs-lookup"><span data-stu-id="d9fb4-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d9fb4-112">Neste exemplo, vamos parar uma sessão de captura de pacote em execução chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="d9fb4-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="d9fb4-113">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d9fb4-114">OS</span><span class="sxs-lookup"><span data-stu-id="d9fb4-114">PARAMETERS</span></span>

### <span data-ttu-id="d9fb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9fb4-115">-AsJob</span></span>
<span data-ttu-id="d9fb4-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d9fb4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9fb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fb4-117">-DefaultProfile</span></span>
<span data-ttu-id="d9fb4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9fb4-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9fb4-119">-NetworkWatcher</span></span>
<span data-ttu-id="d9fb4-120">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="d9fb4-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d9fb4-121">-NetworkWatcherName</span></span>
<span data-ttu-id="d9fb4-122">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="d9fb4-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d9fb4-123">-PacketCaptureName</span></span>
<span data-ttu-id="d9fb4-124">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-124">The packet capture name.</span></span>

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

### <span data-ttu-id="d9fb4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9fb4-125">-PassThru</span></span>
<span data-ttu-id="d9fb4-126">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="d9fb4-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d9fb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9fb4-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d9fb4-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9fb4-129">-Confirm</span></span>
<span data-ttu-id="d9fb4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9fb4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9fb4-131">-WhatIf</span></span>
<span data-ttu-id="d9fb4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9fb4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9fb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fb4-134">CommonParameters</span></span>
<span data-ttu-id="d9fb4-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9fb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fb4-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fb4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fb4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9fb4-137">INPUTS</span></span>

### <span data-ttu-id="d9fb4-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9fb4-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d9fb4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d9fb4-139">System.String</span></span>

## <span data-ttu-id="d9fb4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9fb4-140">OUTPUTS</span></span>

### <span data-ttu-id="d9fb4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9fb4-141">System.Boolean</span></span>

## <span data-ttu-id="d9fb4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9fb4-142">NOTES</span></span>
<span data-ttu-id="d9fb4-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="d9fb4-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d9fb4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9fb4-144">RELATED LINKS</span></span>

[<span data-ttu-id="d9fb4-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9fb4-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9fb4-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d9fb4-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d9fb4-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9fb4-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9fb4-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9fb4-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9fb4-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9fb4-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9fb4-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9fb4-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9fb4-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9fb4-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9fb4-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d9fb4-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d9fb4-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d9fb4-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d9fb4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d9fb4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d9fb4-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d9fb4-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d9fb4-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d9fb4-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
