---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775502"
---
# <span data-ttu-id="34c76-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="34c76-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="34c76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34c76-102">SYNOPSIS</span></span>
<span data-ttu-id="34c76-103">Exiba as regras de grupo de segurança de rede efetivas e configuradas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="34c76-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="34c76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34c76-104">SYNTAX</span></span>

### <span data-ttu-id="34c76-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="34c76-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c76-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="34c76-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c76-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34c76-107">DESCRIPTION</span></span>
<span data-ttu-id="34c76-108">O Get-AzNetworkWatcherSecurityGroupView permite que você veja as regras de grupo de segurança de rede configuradas e efetivas aplicadas em uma VM.</span><span class="sxs-lookup"><span data-stu-id="34c76-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="34c76-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34c76-109">EXAMPLES</span></span>

### <span data-ttu-id="34c76-110">---Exemplo 1: fazer uma chamada de exibição de grupo de segurança em uma VM---</span><span class="sxs-lookup"><span data-stu-id="34c76-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="34c76-111">No exemplo acima, obtemos primeiro o Inspetor de rede regional e, em seguida, uma VM na região.</span><span class="sxs-lookup"><span data-stu-id="34c76-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="34c76-112">Em seguida, fazemos uma chamada de exibição de grupo de segurança na VM especificada.</span><span class="sxs-lookup"><span data-stu-id="34c76-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="34c76-113">OS</span><span class="sxs-lookup"><span data-stu-id="34c76-113">PARAMETERS</span></span>

### <span data-ttu-id="34c76-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34c76-114">-AsJob</span></span>
<span data-ttu-id="34c76-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="34c76-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34c76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c76-116">-DefaultProfile</span></span>
<span data-ttu-id="34c76-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34c76-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c76-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c76-118">-NetworkWatcher</span></span>
<span data-ttu-id="34c76-119">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="34c76-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="34c76-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="34c76-120">-NetworkWatcherName</span></span>
<span data-ttu-id="34c76-121">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="34c76-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="34c76-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c76-122">-ResourceGroupName</span></span>
<span data-ttu-id="34c76-123">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="34c76-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="34c76-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="34c76-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="34c76-125">A ID da VM de destino</span><span class="sxs-lookup"><span data-stu-id="34c76-125">The target VM Id</span></span>

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

### <span data-ttu-id="34c76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c76-126">CommonParameters</span></span>
<span data-ttu-id="34c76-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c76-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c76-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c76-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34c76-129">INPUTS</span></span>

### <span data-ttu-id="34c76-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c76-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="34c76-131">System. String</span><span class="sxs-lookup"><span data-stu-id="34c76-131">System.String</span></span>

## <span data-ttu-id="34c76-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34c76-132">OUTPUTS</span></span>

### <span data-ttu-id="34c76-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="34c76-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="34c76-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34c76-134">NOTES</span></span>
<span data-ttu-id="34c76-135">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="34c76-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="34c76-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34c76-136">RELATED LINKS</span></span>

[<span data-ttu-id="34c76-137">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c76-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="34c76-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c76-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="34c76-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c76-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="34c76-140">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="34c76-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="34c76-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="34c76-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="34c76-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="34c76-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="34c76-143">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="34c76-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="34c76-144">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c76-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c76-145">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="34c76-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="34c76-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c76-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c76-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c76-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c76-148">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c76-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

