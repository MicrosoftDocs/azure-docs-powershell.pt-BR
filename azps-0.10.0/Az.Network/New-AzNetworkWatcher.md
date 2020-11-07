---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775371"
---
# <span data-ttu-id="e7f9f-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7f9f-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="e7f9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f9f-103">Cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="e7f9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7f9f-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f9f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f9f-106">O cmdlet New-AzNetworkWatcher cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="e7f9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7f9f-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f9f-108">Exemplo 1: criar um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e7f9f-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="e7f9f-109">Este exemplo cria um novo inspetor de rede dentro de um grupo de recursos recém-criado.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="e7f9f-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="e7f9f-111">OS</span><span class="sxs-lookup"><span data-stu-id="e7f9f-111">PARAMETERS</span></span>

### <span data-ttu-id="e7f9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f9f-112">-DefaultProfile</span></span>
<span data-ttu-id="e7f9f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f9f-114">-Local</span><span class="sxs-lookup"><span data-stu-id="e7f9f-114">-Location</span></span>
<span data-ttu-id="e7f9f-115">Ponto.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-115">Location.</span></span>

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

### <span data-ttu-id="e7f9f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7f9f-116">-Name</span></span>
<span data-ttu-id="e7f9f-117">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-117">The network watcher name.</span></span>

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

### <span data-ttu-id="e7f9f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f9f-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7f9f-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-119">The resource group name.</span></span>

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

### <span data-ttu-id="e7f9f-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="e7f9f-120">-Tag</span></span>
<span data-ttu-id="e7f9f-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7f9f-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e7f9f-122">For example:</span></span>

<span data-ttu-id="e7f9f-123">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7f9f-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9f-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7f9f-124">-Confirm</span></span>
<span data-ttu-id="e7f9f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f9f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f9f-126">-WhatIf</span></span>
<span data-ttu-id="e7f9f-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f9f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f9f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f9f-129">CommonParameters</span></span>
<span data-ttu-id="e7f9f-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f9f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f9f-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f9f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f9f-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7f9f-132">INPUTS</span></span>

### <span data-ttu-id="e7f9f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f9f-133">System.String</span></span>
<span data-ttu-id="e7f9f-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7f9f-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7f9f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7f9f-135">OUTPUTS</span></span>

### <span data-ttu-id="e7f9f-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7f9f-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="e7f9f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7f9f-137">NOTES</span></span>
<span data-ttu-id="e7f9f-138">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e7f9f-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e7f9f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7f9f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e7f9f-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7f9f-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e7f9f-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7f9f-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e7f9f-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e7f9f-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e7f9f-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9f-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e7f9f-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e7f9f-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e7f9f-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e7f9f-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e7f9f-146">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e7f9f-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e7f9f-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e7f9f-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e7f9f-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e7f9f-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e7f9f-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e7f9f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e7f9f-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e7f9f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e7f9f-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e7f9f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
