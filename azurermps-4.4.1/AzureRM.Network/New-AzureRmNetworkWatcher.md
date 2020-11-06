---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429264"
---
# <span data-ttu-id="65ea5-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ea5-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="65ea5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="65ea5-103">Cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="65ea5-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ea5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65ea5-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ea5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="65ea5-106">O cmdlet New-AzureRmNetworkWatcher cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="65ea5-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="65ea5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="65ea5-108">Exemplo 1: criar um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="65ea5-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="65ea5-109">Este exemplo cria um novo inspetor de rede dentro de um grupo de recursos recém-criado.</span><span class="sxs-lookup"><span data-stu-id="65ea5-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="65ea5-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="65ea5-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="65ea5-111">OS</span><span class="sxs-lookup"><span data-stu-id="65ea5-111">PARAMETERS</span></span>

### <span data-ttu-id="65ea5-112">-Local</span><span class="sxs-lookup"><span data-stu-id="65ea5-112">-Location</span></span>
<span data-ttu-id="65ea5-113">Ponto.</span><span class="sxs-lookup"><span data-stu-id="65ea5-113">Location.</span></span>

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

### <span data-ttu-id="65ea5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="65ea5-114">-Name</span></span>
<span data-ttu-id="65ea5-115">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="65ea5-115">The network watcher name.</span></span>

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

### <span data-ttu-id="65ea5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ea5-116">-ResourceGroupName</span></span>
<span data-ttu-id="65ea5-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65ea5-117">The resource group name.</span></span>

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

### <span data-ttu-id="65ea5-118">-Marca</span><span class="sxs-lookup"><span data-stu-id="65ea5-118">-Tag</span></span>
<span data-ttu-id="65ea5-119">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="65ea5-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65ea5-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="65ea5-120">For example:</span></span>

<span data-ttu-id="65ea5-121">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="65ea5-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ea5-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65ea5-122">-Confirm</span></span>
<span data-ttu-id="65ea5-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ea5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ea5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ea5-124">-WhatIf</span></span>
<span data-ttu-id="65ea5-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65ea5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ea5-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65ea5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ea5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ea5-127">-DefaultProfile</span></span>
<span data-ttu-id="65ea5-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65ea5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ea5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ea5-129">CommonParameters</span></span>
<span data-ttu-id="65ea5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ea5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ea5-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ea5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ea5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65ea5-132">INPUTS</span></span>

### <span data-ttu-id="65ea5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65ea5-133">System.String</span></span>
<span data-ttu-id="65ea5-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65ea5-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65ea5-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65ea5-135">OUTPUTS</span></span>

### <span data-ttu-id="65ea5-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ea5-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="65ea5-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65ea5-137">NOTES</span></span>
<span data-ttu-id="65ea5-138">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="65ea5-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="65ea5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65ea5-139">RELATED LINKS</span></span>

[<span data-ttu-id="65ea5-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ea5-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="65ea5-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ea5-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="65ea5-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ea5-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ea5-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="65ea5-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="65ea5-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ea5-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ea5-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ea5-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ea5-146">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ea5-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ea5-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="65ea5-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="65ea5-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="65ea5-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="65ea5-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="65ea5-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="65ea5-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="65ea5-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="65ea5-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="65ea5-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
