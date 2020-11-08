---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125562"
---
# <span data-ttu-id="bc243-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-101">Set-AzFirewall</span></span>

## <span data-ttu-id="bc243-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc243-102">SYNOPSIS</span></span>
<span data-ttu-id="bc243-103">Salva um firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="bc243-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="bc243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc243-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc243-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc243-105">DESCRIPTION</span></span>
<span data-ttu-id="bc243-106">O cmdlet **set-AzFirewall** atualiza um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc243-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="bc243-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc243-107">EXAMPLES</span></span>

### <span data-ttu-id="bc243-108">1: atualizar a prioridade de um conjunto de regras de aplicativo de firewall</span><span class="sxs-lookup"><span data-stu-id="bc243-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="bc243-109">Este exemplo atualiza a prioridade de um conjunto de regras existente de um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc243-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="bc243-110">Pressupondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "RG" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente.</span><span class="sxs-lookup"><span data-stu-id="bc243-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="bc243-111">Sem o comando Set-AzFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.</span><span class="sxs-lookup"><span data-stu-id="bc243-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="bc243-112">2: criar um firewall do Azure e definir uma coleção de regras de aplicativo mais tarde</span><span class="sxs-lookup"><span data-stu-id="bc243-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-113">Neste exemplo, um firewall é criado primeiro sem nenhuma coleção de regras de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc243-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="bc243-114">Posteriormente, uma regra de aplicativo e uma coleção de regras de aplicativo são criadas, o objeto de firewall é modificado na memória, sem afetar a configuração real na nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc243-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="bc243-115">Para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="bc243-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="bc243-116">3: atualizar a ameaça do modo de operação da Intel do firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="bc243-117">Este exemplo atualiza o modo de operação de ameaças da Intel do firewall do Azure "AzureFirewall" no grupo de recursos "RG".</span><span class="sxs-lookup"><span data-stu-id="bc243-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="bc243-118">Sem o comando Set-AzFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.</span><span class="sxs-lookup"><span data-stu-id="bc243-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="bc243-119">4: desatribuir e alocar o firewall</span><span class="sxs-lookup"><span data-stu-id="bc243-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="bc243-120">Este exemplo recupera um firewall, desatribui o firewall e salva-o.</span><span class="sxs-lookup"><span data-stu-id="bc243-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="bc243-121">O comando DEALLOCATE remove o serviço em execução, mas preserva a configuração do firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="bc243-122">Para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="bc243-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="bc243-123">Se o usuário quiser iniciar o serviço novamente, o método de alocação deve ser chamado no firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="bc243-124">O novo VNet e o IP público devem estar no mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="bc243-125">Novamente, para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="bc243-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="bc243-126">5: atribuir com um endereço IP público de gerenciamento para cenários de encapsulamento forçado</span><span class="sxs-lookup"><span data-stu-id="bc243-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="bc243-127">Este exemplo aloca o firewall com um endereço IP público de gerenciamento e uma sub-rede para cenários de encapsulamento forçado.</span><span class="sxs-lookup"><span data-stu-id="bc243-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="bc243-128">A VNet deve conter uma sub-rede chamada "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="bc243-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="bc243-129">6: adicionar um endereço IP público a um firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-130">Neste exemplo, o endereço IP público "azFwPublicIp1" como anexado ao firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="bc243-131">7: remover um endereço IP público de um firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-132">Neste exemplo, o endereço IP público "azFwPublicIp1" como separado do firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="bc243-133">8: alterar o endereço IP público de gerenciamento em um firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-134">Neste exemplo, o endereço IP público de gerenciamento do firewall será alterado para "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="bc243-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="bc243-135">9: adicionar a configuração de DNS a um firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-136">Neste exemplo, o proxy DNS e a configuração do servidor DNS estão conectados ao firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="bc243-137">10: Atualize o destino de uma regra existente dentro de um conjunto de regras de aplicativo de firewall</span><span class="sxs-lookup"><span data-stu-id="bc243-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="bc243-138">Este exemplo atualiza o destino de uma regra existente dentro de uma coleção de regras de um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc243-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="bc243-139">Isso permite que você atualize automaticamente suas regras quando endereços IP são alterados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="bc243-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="bc243-140">11: permitir FTP ativo no firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bc243-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="bc243-141">Neste exemplo, o FTP ativo é permitido no firewall.</span><span class="sxs-lookup"><span data-stu-id="bc243-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="bc243-142">OS</span><span class="sxs-lookup"><span data-stu-id="bc243-142">PARAMETERS</span></span>

### <span data-ttu-id="bc243-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc243-143">-AsJob</span></span>
<span data-ttu-id="bc243-144">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bc243-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc243-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-145">-AzureFirewall</span></span>
<span data-ttu-id="bc243-146">O AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc243-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc243-147">-DefaultProfile</span></span>
<span data-ttu-id="bc243-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc243-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc243-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc243-149">-Confirm</span></span>
<span data-ttu-id="bc243-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc243-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc243-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc243-151">-WhatIf</span></span>
<span data-ttu-id="bc243-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc243-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc243-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc243-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc243-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc243-154">CommonParameters</span></span>
<span data-ttu-id="bc243-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc243-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc243-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc243-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc243-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc243-157">INPUTS</span></span>

### <span data-ttu-id="bc243-158">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bc243-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc243-159">OUTPUTS</span></span>

### <span data-ttu-id="bc243-160">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bc243-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc243-161">NOTES</span></span>

## <span data-ttu-id="bc243-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc243-162">RELATED LINKS</span></span>

[<span data-ttu-id="bc243-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="bc243-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="bc243-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc243-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
