---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427826"
---
# <span data-ttu-id="53bc2-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53bc2-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="53bc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="53bc2-103">Interrompe uma sessão de captura de pacote em execução</span><span class="sxs-lookup"><span data-stu-id="53bc2-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53bc2-104">SYNTAX</span></span>

### <span data-ttu-id="53bc2-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="53bc2-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bc2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="53bc2-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53bc2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53bc2-107">DESCRIPTION</span></span>
<span data-ttu-id="53bc2-108">O Stop-AzureRmNetworkWatcherPacketCapture para de uma sessão de captura de pacote em execução.</span><span class="sxs-lookup"><span data-stu-id="53bc2-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="53bc2-109">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="53bc2-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="53bc2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53bc2-110">EXAMPLES</span></span>

### <span data-ttu-id="53bc2-111">---Exemplo 1: parar uma sessão de captura de pacote---</span><span class="sxs-lookup"><span data-stu-id="53bc2-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="53bc2-112">Neste exemplo, vamos parar uma sessão de captura de pacote em execução chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="53bc2-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="53bc2-113">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="53bc2-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="53bc2-114">OS</span><span class="sxs-lookup"><span data-stu-id="53bc2-114">PARAMETERS</span></span>

### <span data-ttu-id="53bc2-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53bc2-115">-NetworkWatcher</span></span>
<span data-ttu-id="53bc2-116">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="53bc2-116">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="53bc2-117">-NetworkWatcherName</span></span>
<span data-ttu-id="53bc2-118">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="53bc2-118">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="53bc2-119">-PacketCaptureName</span></span>
<span data-ttu-id="53bc2-120">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="53bc2-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53bc2-121">-PassThru</span></span>
<span data-ttu-id="53bc2-122">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="53bc2-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bc2-123">-ResourceGroupName</span></span>
<span data-ttu-id="53bc2-124">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="53bc2-124">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53bc2-125">-Confirm</span></span>
<span data-ttu-id="53bc2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53bc2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bc2-127">-WhatIf</span></span>
<span data-ttu-id="53bc2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53bc2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53bc2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53bc2-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bc2-130">-DefaultProfile</span></span>
<span data-ttu-id="53bc2-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53bc2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bc2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bc2-132">CommonParameters</span></span>
<span data-ttu-id="53bc2-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bc2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bc2-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bc2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bc2-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53bc2-135">INPUTS</span></span>

### <span data-ttu-id="53bc2-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53bc2-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="53bc2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53bc2-137">System.String</span></span>

## <span data-ttu-id="53bc2-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53bc2-138">OUTPUTS</span></span>

### <span data-ttu-id="53bc2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53bc2-139">System.Boolean</span></span>

## <span data-ttu-id="53bc2-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53bc2-140">NOTES</span></span>
<span data-ttu-id="53bc2-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="53bc2-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="53bc2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53bc2-142">RELATED LINKS</span></span>

[<span data-ttu-id="53bc2-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53bc2-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53bc2-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="53bc2-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="53bc2-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53bc2-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53bc2-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="53bc2-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="53bc2-147">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53bc2-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53bc2-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53bc2-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53bc2-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="53bc2-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="53bc2-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="53bc2-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="53bc2-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="53bc2-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="53bc2-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="53bc2-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="53bc2-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="53bc2-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="53bc2-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="53bc2-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
