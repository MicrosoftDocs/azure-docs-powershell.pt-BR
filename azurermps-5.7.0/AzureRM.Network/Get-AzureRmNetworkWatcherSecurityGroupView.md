---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 5b48cbabfe91b16924a1296a73354db659ec8f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610926"
---
# <span data-ttu-id="b2851-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b2851-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="b2851-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2851-102">SYNOPSIS</span></span>
<span data-ttu-id="b2851-103">Exiba as regras de grupo de segurança de rede efetivas e configuradas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="b2851-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2851-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2851-104">SYNTAX</span></span>

### <span data-ttu-id="b2851-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2851-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2851-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b2851-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2851-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2851-107">DESCRIPTION</span></span>
<span data-ttu-id="b2851-108">O Get-AzureRmNetworkWatcherSecurityGroupView permite que você veja as regras de grupo de segurança de rede configuradas e efetivas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="b2851-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b2851-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2851-109">EXAMPLES</span></span>

### <span data-ttu-id="b2851-110">---Exemplo 1: fazer uma chamada de exibição de grupo de segurança em uma VM---</span><span class="sxs-lookup"><span data-stu-id="b2851-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="b2851-111">No exemplo acima, obtemos primeiro o Inspetor de rede regional e, em seguida, uma VM na região.</span><span class="sxs-lookup"><span data-stu-id="b2851-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="b2851-112">Em seguida, fazemos uma chamada de exibição de grupo de segurança na VM especificada.</span><span class="sxs-lookup"><span data-stu-id="b2851-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="b2851-113">OS</span><span class="sxs-lookup"><span data-stu-id="b2851-113">PARAMETERS</span></span>

### <span data-ttu-id="b2851-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2851-114">-AsJob</span></span>
<span data-ttu-id="b2851-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2851-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2851-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2851-116">-DefaultProfile</span></span>
<span data-ttu-id="b2851-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2851-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2851-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2851-118">-NetworkWatcher</span></span>
<span data-ttu-id="b2851-119">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b2851-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="b2851-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b2851-120">-NetworkWatcherName</span></span>
<span data-ttu-id="b2851-121">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b2851-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="b2851-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2851-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2851-123">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b2851-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b2851-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b2851-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b2851-125">A ID da VM de destino</span><span class="sxs-lookup"><span data-stu-id="b2851-125">The target VM Id</span></span>

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

### <span data-ttu-id="b2851-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2851-126">CommonParameters</span></span>
<span data-ttu-id="b2851-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2851-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2851-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2851-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2851-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2851-129">INPUTS</span></span>

### <span data-ttu-id="b2851-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2851-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b2851-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2851-131">System.String</span></span>

## <span data-ttu-id="b2851-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2851-132">OUTPUTS</span></span>

### <span data-ttu-id="b2851-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="b2851-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="b2851-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2851-134">NOTES</span></span>
<span data-ttu-id="b2851-135">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="b2851-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="b2851-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2851-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2851-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2851-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2851-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2851-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2851-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2851-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2851-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b2851-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b2851-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b2851-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b2851-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b2851-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b2851-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b2851-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b2851-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2851-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2851-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b2851-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b2851-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2851-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2851-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2851-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2851-148">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2851-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

