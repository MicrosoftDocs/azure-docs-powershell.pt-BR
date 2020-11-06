---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432182"
---
# <span data-ttu-id="1c0ff-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1c0ff-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="1c0ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0ff-103">Exiba as regras de grupo de segurança de rede efetivas e configuradas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c0ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c0ff-104">SYNTAX</span></span>

### <span data-ttu-id="1c0ff-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c0ff-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c0ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1c0ff-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c0ff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c0ff-107">DESCRIPTION</span></span>
<span data-ttu-id="1c0ff-108">O Get-AzureRmNetworkWatcherSecurityGroupView permite que você veja as regras de grupo de segurança de rede configuradas e efetivas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="1c0ff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c0ff-109">EXAMPLES</span></span>

### <span data-ttu-id="1c0ff-110">---Exemplo 1: fazer uma chamada de exibição de grupo de segurança em uma VM---</span><span class="sxs-lookup"><span data-stu-id="1c0ff-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="1c0ff-111">No exemplo acima, obtemos primeiro o Inspetor de rede regional e, em seguida, uma VM na região.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="1c0ff-112">Em seguida, fazemos uma chamada de exibição de grupo de segurança na VM especificada.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="1c0ff-113">OS</span><span class="sxs-lookup"><span data-stu-id="1c0ff-113">PARAMETERS</span></span>

### <span data-ttu-id="1c0ff-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c0ff-114">-NetworkWatcher</span></span>
<span data-ttu-id="1c0ff-115">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-115">The network watcher resource.</span></span>

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

### <span data-ttu-id="1c0ff-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1c0ff-116">-NetworkWatcherName</span></span>
<span data-ttu-id="1c0ff-117">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-117">The name of network watcher.</span></span>

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

### <span data-ttu-id="1c0ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c0ff-119">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-119">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1c0ff-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1c0ff-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1c0ff-121">A ID da VM de destino</span><span class="sxs-lookup"><span data-stu-id="1c0ff-121">The target VM Id</span></span>

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

### <span data-ttu-id="1c0ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0ff-122">-DefaultProfile</span></span>
<span data-ttu-id="1c0ff-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c0ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0ff-124">CommonParameters</span></span>
<span data-ttu-id="1c0ff-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0ff-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0ff-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c0ff-127">INPUTS</span></span>

### <span data-ttu-id="1c0ff-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c0ff-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1c0ff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1c0ff-129">System.String</span></span>

## <span data-ttu-id="1c0ff-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c0ff-130">OUTPUTS</span></span>

### <span data-ttu-id="1c0ff-131">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="1c0ff-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="1c0ff-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c0ff-132">NOTES</span></span>
<span data-ttu-id="1c0ff-133">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="1c0ff-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="1c0ff-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c0ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c0ff-135">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c0ff-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1c0ff-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c0ff-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1c0ff-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c0ff-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1c0ff-138">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1c0ff-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1c0ff-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1c0ff-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1c0ff-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1c0ff-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1c0ff-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1c0ff-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1c0ff-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c0ff-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c0ff-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1c0ff-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1c0ff-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c0ff-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c0ff-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c0ff-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c0ff-146">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c0ff-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

