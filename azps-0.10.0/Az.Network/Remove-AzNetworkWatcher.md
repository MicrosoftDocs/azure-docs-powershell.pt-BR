---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776622"
---
# <span data-ttu-id="23c98-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c98-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="23c98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23c98-102">SYNOPSIS</span></span>
<span data-ttu-id="23c98-103">Remove um inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="23c98-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="23c98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23c98-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23c98-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23c98-105">DESCRIPTION</span></span>
<span data-ttu-id="23c98-106">O cmdlet Remove-AzNetworkWatcher remove um recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="23c98-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="23c98-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23c98-107">EXAMPLES</span></span>

### <span data-ttu-id="23c98-108">--------------------------Exemplo 1: criar e excluir um inspetor de rede--------------------------</span><span class="sxs-lookup"><span data-stu-id="23c98-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="23c98-109">Este exemplo cria um inspetor de rede em um grupo de recursos e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="23c98-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="23c98-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="23c98-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="23c98-111">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="23c98-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="23c98-112">OS</span><span class="sxs-lookup"><span data-stu-id="23c98-112">PARAMETERS</span></span>

### <span data-ttu-id="23c98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23c98-113">-AsJob</span></span>
<span data-ttu-id="23c98-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23c98-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23c98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c98-115">-DefaultProfile</span></span>
<span data-ttu-id="23c98-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23c98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23c98-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="23c98-117">-Name</span></span>
<span data-ttu-id="23c98-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="23c98-118">The resource name.</span></span>

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

### <span data-ttu-id="23c98-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23c98-119">-PassThru</span></span>
<span data-ttu-id="23c98-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="23c98-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="23c98-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c98-121">-ResourceGroupName</span></span>
<span data-ttu-id="23c98-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23c98-122">The resource group name.</span></span>

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

### <span data-ttu-id="23c98-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23c98-123">-Confirm</span></span>
<span data-ttu-id="23c98-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23c98-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c98-125">-WhatIf</span></span>
<span data-ttu-id="23c98-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23c98-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23c98-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23c98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23c98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c98-128">CommonParameters</span></span>
<span data-ttu-id="23c98-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c98-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c98-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c98-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23c98-131">INPUTS</span></span>

### <span data-ttu-id="23c98-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23c98-132">System.String</span></span>

## <span data-ttu-id="23c98-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23c98-133">OUTPUTS</span></span>

### <span data-ttu-id="23c98-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="23c98-134">System.Object</span></span>

## <span data-ttu-id="23c98-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23c98-135">NOTES</span></span>
<span data-ttu-id="23c98-136">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="23c98-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="23c98-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23c98-137">RELATED LINKS</span></span>

[<span data-ttu-id="23c98-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c98-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="23c98-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c98-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="23c98-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c98-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c98-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="23c98-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="23c98-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c98-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c98-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c98-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c98-144">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c98-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c98-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="23c98-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="23c98-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="23c98-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="23c98-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="23c98-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="23c98-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="23c98-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="23c98-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="23c98-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
