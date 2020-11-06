---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440760"
---
# <span data-ttu-id="ad114-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad114-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="ad114-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad114-102">SYNOPSIS</span></span>
<span data-ttu-id="ad114-103">Cria um novo firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad114-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad114-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad114-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad114-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad114-105">DESCRIPTION</span></span>
<span data-ttu-id="ad114-106">O cmdlet **New-AzureRmFirewall** cria um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad114-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="ad114-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad114-107">EXAMPLES</span></span>

### <span data-ttu-id="ad114-108">1: criar um firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="ad114-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="ad114-109">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="ad114-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ad114-110">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="ad114-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="ad114-111">2: criar um firewall que permita todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="ad114-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="ad114-112">Este exemplo cria um firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="ad114-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="ad114-113">3: DNAT-redirecionar o tráfego destinado ao 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="ad114-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="ad114-114">Este exemplo criou um firewall que converteu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="ad114-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="ad114-115">OS</span><span class="sxs-lookup"><span data-stu-id="ad114-115">PARAMETERS</span></span>

### <span data-ttu-id="ad114-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="ad114-117">Especifica as coleções de regras do aplicativo para o novo firewall.</span><span class="sxs-lookup"><span data-stu-id="ad114-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad114-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad114-118">-AsJob</span></span>
<span data-ttu-id="ad114-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ad114-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad114-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad114-120">-DefaultProfile</span></span>
<span data-ttu-id="ad114-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad114-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad114-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ad114-122">-Force</span></span>
<span data-ttu-id="ad114-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad114-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad114-124">-Local</span><span class="sxs-lookup"><span data-stu-id="ad114-124">-Location</span></span>
<span data-ttu-id="ad114-125">Especifica a região do firewall.</span><span class="sxs-lookup"><span data-stu-id="ad114-125">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="ad114-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad114-126">-Name</span></span>
<span data-ttu-id="ad114-127">Especifica o nome do firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="ad114-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ad114-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-128">-NatRuleCollection</span></span>
<span data-ttu-id="ad114-129">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="ad114-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad114-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="ad114-131">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="ad114-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad114-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="ad114-132">-PublicIpName</span></span>
<span data-ttu-id="ad114-133">Nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="ad114-133">Public Ip Name.</span></span> <span data-ttu-id="ad114-134">O IP público deve usar a SKU padrão e deve pertencer ao mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="ad114-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad114-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad114-135">-ResourceGroupName</span></span>
<span data-ttu-id="ad114-136">Especifica o nome de um grupo de recursos para conter o firewall.</span><span class="sxs-lookup"><span data-stu-id="ad114-136">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="ad114-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="ad114-137">-Tag</span></span>
<span data-ttu-id="ad114-138">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ad114-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ad114-139">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ad114-139">For example:</span></span>

<span data-ttu-id="ad114-140">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ad114-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ad114-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ad114-141">-VirtualNetworkName</span></span>
<span data-ttu-id="ad114-142">Especifica o nome da rede virtual para a qual o firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="ad114-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="ad114-143">A rede virtual e o firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad114-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad114-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad114-144">-Confirm</span></span>
<span data-ttu-id="ad114-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad114-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad114-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad114-146">-WhatIf</span></span>
<span data-ttu-id="ad114-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad114-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad114-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad114-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad114-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad114-149">CommonParameters</span></span>
<span data-ttu-id="ad114-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad114-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad114-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad114-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad114-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad114-152">INPUTS</span></span>

### <span data-ttu-id="ad114-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ad114-153">None</span></span>
<span data-ttu-id="ad114-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ad114-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad114-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad114-155">OUTPUTS</span></span>

### <span data-ttu-id="ad114-156">Microsoft. Azure. Commands. Network. Models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="ad114-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="ad114-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad114-157">NOTES</span></span>

## <span data-ttu-id="ad114-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad114-158">RELATED LINKS</span></span>

[<span data-ttu-id="ad114-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad114-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="ad114-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad114-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="ad114-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad114-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="ad114-162">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="ad114-163">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="ad114-164">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad114-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
