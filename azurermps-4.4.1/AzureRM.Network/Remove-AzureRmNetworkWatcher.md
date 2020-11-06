---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426882"
---
# <span data-ttu-id="02f9b-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02f9b-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="02f9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="02f9b-103">Remove um inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="02f9b-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02f9b-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="02f9b-106">O cmdlet Remove-AzureRmNetworkWatcher remove um recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="02f9b-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="02f9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="02f9b-108">--------------------------Exemplo 1: criar e excluir um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="02f9b-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="02f9b-109">Este exemplo cria um inspetor de rede em um grupo de recursos e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="02f9b-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="02f9b-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="02f9b-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="02f9b-111">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="02f9b-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="02f9b-112">OS</span><span class="sxs-lookup"><span data-stu-id="02f9b-112">PARAMETERS</span></span>

### <span data-ttu-id="02f9b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="02f9b-113">-Name</span></span>
<span data-ttu-id="02f9b-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="02f9b-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f9b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02f9b-115">-PassThru</span></span>
<span data-ttu-id="02f9b-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="02f9b-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="02f9b-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02f9b-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f9b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02f9b-119">-Confirm</span></span>
<span data-ttu-id="02f9b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f9b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f9b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f9b-121">-WhatIf</span></span>
<span data-ttu-id="02f9b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02f9b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f9b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02f9b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f9b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f9b-124">-DefaultProfile</span></span>
<span data-ttu-id="02f9b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02f9b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f9b-126">CommonParameters</span></span>
<span data-ttu-id="02f9b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f9b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f9b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f9b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02f9b-129">INPUTS</span></span>

### <span data-ttu-id="02f9b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02f9b-130">System.String</span></span>

## <span data-ttu-id="02f9b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02f9b-131">OUTPUTS</span></span>

### <span data-ttu-id="02f9b-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="02f9b-132">System.Object</span></span>

## <span data-ttu-id="02f9b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02f9b-133">NOTES</span></span>
<span data-ttu-id="02f9b-134">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="02f9b-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="02f9b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02f9b-135">RELATED LINKS</span></span>

[<span data-ttu-id="02f9b-136">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02f9b-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="02f9b-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02f9b-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="02f9b-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02f9b-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02f9b-139">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="02f9b-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="02f9b-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02f9b-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02f9b-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02f9b-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02f9b-142">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02f9b-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02f9b-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="02f9b-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="02f9b-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="02f9b-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="02f9b-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="02f9b-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="02f9b-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="02f9b-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="02f9b-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="02f9b-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
