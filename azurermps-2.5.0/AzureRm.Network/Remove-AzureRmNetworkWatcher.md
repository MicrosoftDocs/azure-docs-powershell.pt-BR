---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785886"
---
# <span data-ttu-id="e3521-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3521-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="e3521-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3521-102">SYNOPSIS</span></span>
<span data-ttu-id="e3521-103">Remove um inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e3521-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3521-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3521-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3521-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3521-105">DESCRIPTION</span></span>
<span data-ttu-id="e3521-106">O cmdlet Remove-AzureRmNetworkWatcher remove um recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e3521-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="e3521-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3521-107">EXAMPLES</span></span>

### <span data-ttu-id="e3521-108">--------------------------Exemplo 1: criar e excluir um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3521-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="e3521-109">Este exemplo cria um inspetor de rede em um grupo de recursos e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e3521-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e3521-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3521-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="e3521-111">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="e3521-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e3521-112">OS</span><span class="sxs-lookup"><span data-stu-id="e3521-112">PARAMETERS</span></span>

### <span data-ttu-id="e3521-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3521-113">-AsJob</span></span>
<span data-ttu-id="e3521-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e3521-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3521-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3521-115">-DefaultProfile</span></span>
<span data-ttu-id="e3521-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3521-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3521-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3521-117">-Name</span></span>
<span data-ttu-id="e3521-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3521-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3521-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3521-119">-PassThru</span></span>
<span data-ttu-id="e3521-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e3521-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e3521-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3521-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3521-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3521-122">The resource group name.</span></span>

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

### <span data-ttu-id="e3521-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3521-123">-Confirm</span></span>
<span data-ttu-id="e3521-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3521-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3521-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3521-125">-WhatIf</span></span>
<span data-ttu-id="e3521-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3521-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3521-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3521-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3521-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3521-128">CommonParameters</span></span>
<span data-ttu-id="e3521-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3521-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3521-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3521-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3521-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3521-131">INPUTS</span></span>

### <span data-ttu-id="e3521-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3521-132">System.String</span></span>

## <span data-ttu-id="e3521-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3521-133">OUTPUTS</span></span>

### <span data-ttu-id="e3521-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3521-134">System.Object</span></span>

## <span data-ttu-id="e3521-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3521-135">NOTES</span></span>
<span data-ttu-id="e3521-136">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e3521-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e3521-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3521-137">RELATED LINKS</span></span>

[<span data-ttu-id="e3521-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3521-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e3521-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3521-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e3521-140">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3521-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3521-141">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e3521-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e3521-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3521-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3521-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3521-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3521-144">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3521-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3521-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e3521-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e3521-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e3521-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e3521-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e3521-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e3521-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e3521-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e3521-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e3521-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
