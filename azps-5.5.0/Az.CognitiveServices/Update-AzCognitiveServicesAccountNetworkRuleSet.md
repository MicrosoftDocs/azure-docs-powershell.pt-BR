---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117888"
---
# <span data-ttu-id="11e65-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11e65-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="11e65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11e65-102">SYNOPSIS</span></span>
<span data-ttu-id="11e65-103">Atualizar a propriedade NetworkRule de uma conta do Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="11e65-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="11e65-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11e65-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11e65-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11e65-105">DESCRIPTION</span></span>
<span data-ttu-id="11e65-106">O cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta do Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="11e65-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="11e65-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11e65-107">EXAMPLES</span></span>

### <span data-ttu-id="11e65-108">Exemplo 1: Atualizar todas as propriedades do NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="11e65-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="11e65-109">Este comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="11e65-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="11e65-110">Exemplo 2: atualizar a propriedade Bypass da NetworkRule</span><span class="sxs-lookup"><span data-stu-id="11e65-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="11e65-111">Esta propriedade de atualização de comando Bypass da NetworkRule (outras propriedades não mudarão).</span><span class="sxs-lookup"><span data-stu-id="11e65-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="11e65-112">Exemplo 3: Limpar regras de NetworkRule de uma conta dos Serviços Cognitivas</span><span class="sxs-lookup"><span data-stu-id="11e65-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="11e65-113">Este comando limpa as regras de NetworkRule de uma conta dos Serviços Cognitivas (outras propriedades não mudam).</span><span class="sxs-lookup"><span data-stu-id="11e65-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="11e65-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e65-114">PARAMETERS</span></span>

### <span data-ttu-id="11e65-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="11e65-115">-DefaultAction</span></span>
<span data-ttu-id="11e65-116">NetworkRule DefaultAction da Conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="11e65-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="11e65-117">Valor `Deny` padrão.</span><span class="sxs-lookup"><span data-stu-id="11e65-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e65-118">-DefaultProfile</span></span>
<span data-ttu-id="11e65-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11e65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e65-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="11e65-120">-IpRule</span></span>
<span data-ttu-id="11e65-121">IpRules networkrule da conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="11e65-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e65-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="11e65-122">-Name</span></span>
<span data-ttu-id="11e65-123">Nome da conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="11e65-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e65-124">-ResourceGroupName</span></span>
<span data-ttu-id="11e65-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11e65-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e65-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11e65-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="11e65-127">Conta cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="11e65-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e65-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11e65-128">-Confirm</span></span>
<span data-ttu-id="11e65-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e65-130">-WhatIf</span></span>
<span data-ttu-id="11e65-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11e65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e65-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11e65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e65-133">CommonParameters</span></span>
<span data-ttu-id="11e65-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e65-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11e65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e65-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="11e65-136">INPUTS</span></span>

### <span data-ttu-id="11e65-137">System.String</span><span class="sxs-lookup"><span data-stu-id="11e65-137">System.String</span></span>

### <span data-ttu-id="11e65-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="11e65-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="11e65-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="11e65-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="11e65-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="11e65-140">OUTPUTS</span></span>

### <span data-ttu-id="11e65-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11e65-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="11e65-142">Notas</span><span class="sxs-lookup"><span data-stu-id="11e65-142">NOTES</span></span>

## <span data-ttu-id="11e65-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11e65-143">RELATED LINKS</span></span>
