---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114097"
---
# <span data-ttu-id="b1535-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-101">Set-AzFirewall</span></span>

## <span data-ttu-id="b1535-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1535-102">SYNOPSIS</span></span>
<span data-ttu-id="b1535-103">Salva um Firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="b1535-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="b1535-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1535-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1535-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1535-105">DESCRIPTION</span></span>
<span data-ttu-id="b1535-106">O cmdlet **Set-AzFirewall** atualiza um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1535-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="b1535-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1535-107">EXAMPLES</span></span>

### <span data-ttu-id="b1535-108">1: Prioridade de atualização de um conjunto de regras do aplicativo Firewall</span><span class="sxs-lookup"><span data-stu-id="b1535-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="b1535-109">Este exemplo atualiza a prioridade de um conjunto de regras existente de um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1535-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="b1535-110">Supondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "rg" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b1535-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="b1535-111">Sem o Set-AzFirewall, todas as operações executadas no $azFw local não são refletidas no servidor.</span><span class="sxs-lookup"><span data-stu-id="b1535-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="b1535-112">2: Criar um Firewall do Azure e definir uma coleção de regras de aplicativo mais tarde</span><span class="sxs-lookup"><span data-stu-id="b1535-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-113">Neste exemplo, um Firewall é criado primeiro sem nenhum conjunto de regras de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1535-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="b1535-114">Posteriormente, uma Regra de Aplicativo e Um Conjunto de Regras de Aplicativo são criados e, em seguida, o objeto Firewall é modificado na memória, sem afetar a configuração real na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b1535-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="b1535-115">Para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="b1535-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="b1535-116">3: Atualizar o modo de operação Da Intel de Ameaças do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="b1535-117">Este exemplo atualiza o modo de operação de Inteligência contra Ameaças do Firewall do Azure "AzureFirewall" no grupo de recursos "rg".</span><span class="sxs-lookup"><span data-stu-id="b1535-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="b1535-118">Sem o Set-AzFirewall, todas as operações executadas no $azFw local não são refletidas no servidor.</span><span class="sxs-lookup"><span data-stu-id="b1535-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="b1535-119">4: Desloque e aloque o Firewall</span><span class="sxs-lookup"><span data-stu-id="b1535-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="b1535-120">Este exemplo recupera um Firewall, locado o firewall e o salva.</span><span class="sxs-lookup"><span data-stu-id="b1535-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="b1535-121">O comando Deallocate remove o serviço em execução, mas preserva a configuração do firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="b1535-122">Para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="b1535-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="b1535-123">Se o usuário quiser iniciar o serviço novamente, o método Alocar deverá ser chamado no firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="b1535-124">O novo VNet e o IP público devem estar no mesmo grupo de recursos que o Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="b1535-125">Novamente, para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="b1535-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="b1535-126">5: Alocar com um endereço IP público de gerenciamento para cenários de túnel forçado</span><span class="sxs-lookup"><span data-stu-id="b1535-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="b1535-127">Este exemplo aloca o firewall com um endereço IP público de gerenciamento e uma sub-rede para cenários de túnel forçados.</span><span class="sxs-lookup"><span data-stu-id="b1535-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="b1535-128">A VNet deve conter uma sub-rede chamada "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="b1535-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="b1535-129">6: Adicionar um endereço IP público a um Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-130">Neste exemplo, o Endereço IP Público "azFwPublicIp1" conforme anexado ao Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="b1535-131">7: Remover um endereço IP público de um Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-132">Neste exemplo, o Endereço IP Público "azFwPublicIp1" conforme desconectado do Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="b1535-133">8: Alterar o endereço IP público de gerenciamento em um Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-134">Neste exemplo, o endereço IP público de gerenciamento do firewall será alterado para "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="b1535-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="b1535-135">9: Adicionar configuração DNS a um Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-136">Neste exemplo, a configuração do Proxy DNS e do Servidor DNS está anexada ao Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="b1535-137">10: Atualizar o destino de uma regra existente dentro de um conjunto de regras de aplicativo firewall</span><span class="sxs-lookup"><span data-stu-id="b1535-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="b1535-138">Este exemplo atualiza o destino de uma regra existente em um conjunto de regras de um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1535-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="b1535-139">Isso permite que você atualize automaticamente suas regras quando os endereços IP mudarem dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="b1535-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="b1535-140">11: Permitir FTP Ativo no Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1535-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="b1535-141">Neste exemplo, FTP Ativo é permitido no Firewall.</span><span class="sxs-lookup"><span data-stu-id="b1535-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="b1535-142">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1535-142">PARAMETERS</span></span>

### <span data-ttu-id="b1535-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1535-143">-AsJob</span></span>
<span data-ttu-id="b1535-144">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1535-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1535-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-145">-AzureFirewall</span></span>
<span data-ttu-id="b1535-146">O AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="b1535-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1535-147">-DefaultProfile</span></span>
<span data-ttu-id="b1535-148">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b1535-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1535-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b1535-149">-Confirm</span></span>
<span data-ttu-id="b1535-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1535-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1535-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1535-151">-WhatIf</span></span>
<span data-ttu-id="b1535-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b1535-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1535-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1535-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1535-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1535-154">CommonParameters</span></span>
<span data-ttu-id="b1535-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1535-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1535-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1535-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1535-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="b1535-157">INPUTS</span></span>

### <span data-ttu-id="b1535-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b1535-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="b1535-159">OUTPUTS</span></span>

### <span data-ttu-id="b1535-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b1535-161">Notas</span><span class="sxs-lookup"><span data-stu-id="b1535-161">NOTES</span></span>

## <span data-ttu-id="b1535-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1535-162">RELATED LINKS</span></span>

[<span data-ttu-id="b1535-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b1535-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b1535-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1535-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
