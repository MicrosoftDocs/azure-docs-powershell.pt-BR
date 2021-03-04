---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 4c5cd8caef4499d8d603b1947c1fa1dd8a9d5cf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888584"
---
# <span data-ttu-id="e3c1c-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3c1c-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="e3c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c1c-103">Atualizar a propriedade NetworkRule de uma conta dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="e3c1c-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e3c1c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3c1c-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3c1c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c1c-106">O cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="e3c1c-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e3c1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c1c-108">Exemplo 1: Atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="e3c1c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="e3c1c-109">Este comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="e3c1c-110">Exemplo 2: Atualizar a propriedade Bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3c1c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="e3c1c-111">Este comando atualiza a propriedade Bypass de NetworkRule (outras propriedades não mudarão).</span><span class="sxs-lookup"><span data-stu-id="e3c1c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="e3c1c-112">Exemplo 3: Limpar regras de NetworkRule de uma conta dos Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="e3c1c-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="e3c1c-113">Este comando limpa as regras de NetworkRule de uma conta dos Serviços Cognitivos (outras propriedades não mudam).</span><span class="sxs-lookup"><span data-stu-id="e3c1c-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="e3c1c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-114">PARAMETERS</span></span>

### <span data-ttu-id="e3c1c-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="e3c1c-115">-DefaultAction</span></span>
<span data-ttu-id="e3c1c-116">Rede de Contas de Serviços CognitivosRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="e3c1c-117">Valor padrão `Deny` .</span><span class="sxs-lookup"><span data-stu-id="e3c1c-117">Default value `Deny`.</span></span>

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

### <span data-ttu-id="e3c1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c1c-118">-DefaultProfile</span></span>
<span data-ttu-id="e3c1c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c1c-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e3c1c-120">-IpRule</span></span>
<span data-ttu-id="e3c1c-121">Rede de Contas de Serviços CognitivosRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-121">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="e3c1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3c1c-122">-Name</span></span>
<span data-ttu-id="e3c1c-123">Nome da conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="e3c1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3c1c-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e3c1c-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3c1c-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="e3c1c-127">Rede de Contas de Serviços CognitivosRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="e3c1c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c1c-128">-Confirm</span></span>
<span data-ttu-id="e3c1c-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c1c-130">-WhatIf</span></span>
<span data-ttu-id="e3c1c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c1c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c1c-133">CommonParameters</span></span>
<span data-ttu-id="e3c1c-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c1c-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3c1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c1c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-136">INPUTS</span></span>

### <span data-ttu-id="e3c1c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c1c-137">System.String</span></span>

### <span data-ttu-id="e3c1c-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="e3c1c-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e3c1c-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="e3c1c-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e3c1c-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-140">OUTPUTS</span></span>

### <span data-ttu-id="e3c1c-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3c1c-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="e3c1c-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3c1c-142">NOTES</span></span>

## <span data-ttu-id="e3c1c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3c1c-143">RELATED LINKS</span></span>
