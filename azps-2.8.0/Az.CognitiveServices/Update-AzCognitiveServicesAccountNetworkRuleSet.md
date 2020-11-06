---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 114163bdae16d73f490f0110186ccd43bee7d43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597534"
---
# <span data-ttu-id="a5d83-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5d83-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="a5d83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5d83-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d83-103">Atualizar a propriedade NetworkRule de uma conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="a5d83-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a5d83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d83-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5d83-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d83-106">O cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="a5d83-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a5d83-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d83-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d83-108">Exemplo 1: atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="a5d83-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="a5d83-109">Esse comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="a5d83-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="a5d83-110">Exemplo 2: atualizar a propriedade bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5d83-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="a5d83-111">Esta propriedade de atualização de comando bypass de NetworkRule (outras propriedades não se alteram).</span><span class="sxs-lookup"><span data-stu-id="a5d83-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="a5d83-112">Exemplo 3: limpar regras de NetworkRule de uma conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="a5d83-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="a5d83-113">Este comando limpa as regras de NetworkRule de uma conta de serviços cognitiva (outras propriedades não são alteradas).</span><span class="sxs-lookup"><span data-stu-id="a5d83-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="a5d83-114">OS</span><span class="sxs-lookup"><span data-stu-id="a5d83-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d83-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a5d83-115">-DefaultAction</span></span>
<span data-ttu-id="a5d83-116">Conta de serviços cognitiva NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="a5d83-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="a5d83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d83-117">-DefaultProfile</span></span>
<span data-ttu-id="a5d83-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d83-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a5d83-119">-IpRule</span></span>
<span data-ttu-id="a5d83-120">Conta de serviços cognitiva NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="a5d83-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="a5d83-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5d83-121">-Name</span></span>
<span data-ttu-id="a5d83-122">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a5d83-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="a5d83-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d83-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5d83-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5d83-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5d83-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5d83-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="a5d83-126">Conta de serviços cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a5d83-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="a5d83-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5d83-127">-Confirm</span></span>
<span data-ttu-id="a5d83-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d83-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d83-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d83-129">-WhatIf</span></span>
<span data-ttu-id="a5d83-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5d83-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d83-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5d83-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d83-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d83-132">CommonParameters</span></span>
<span data-ttu-id="a5d83-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d83-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d83-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5d83-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d83-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5d83-135">INPUTS</span></span>

### <span data-ttu-id="a5d83-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d83-136">System.String</span></span>

### <span data-ttu-id="a5d83-137">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="a5d83-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a5d83-138">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="a5d83-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a5d83-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5d83-139">OUTPUTS</span></span>

### <span data-ttu-id="a5d83-140">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5d83-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="a5d83-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5d83-141">NOTES</span></span>

## <span data-ttu-id="a5d83-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d83-142">RELATED LINKS</span></span>
