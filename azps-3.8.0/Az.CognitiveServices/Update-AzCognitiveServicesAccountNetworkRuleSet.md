---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 5c01b692e47c3d246982be353093c436a91d6b64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940299"
---
# <span data-ttu-id="daafd-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daafd-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="daafd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daafd-102">SYNOPSIS</span></span>
<span data-ttu-id="daafd-103">Atualizar a propriedade NetworkRule de uma conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="daafd-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="daafd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daafd-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daafd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daafd-105">DESCRIPTION</span></span>
<span data-ttu-id="daafd-106">O cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="daafd-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="daafd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daafd-107">EXAMPLES</span></span>

### <span data-ttu-id="daafd-108">Exemplo 1: atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="daafd-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="daafd-109">Esse comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="daafd-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="daafd-110">Exemplo 2: atualizar a propriedade bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="daafd-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="daafd-111">Esta propriedade de atualização de comando bypass de NetworkRule (outras propriedades não se alteram).</span><span class="sxs-lookup"><span data-stu-id="daafd-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="daafd-112">Exemplo 3: limpar regras de NetworkRule de uma conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="daafd-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="daafd-113">Este comando limpa as regras de NetworkRule de uma conta de serviços cognitiva (outras propriedades não são alteradas).</span><span class="sxs-lookup"><span data-stu-id="daafd-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="daafd-114">OS</span><span class="sxs-lookup"><span data-stu-id="daafd-114">PARAMETERS</span></span>

### <span data-ttu-id="daafd-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="daafd-115">-DefaultAction</span></span>
<span data-ttu-id="daafd-116">Conta de serviços cognitiva NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="daafd-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="daafd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daafd-117">-DefaultProfile</span></span>
<span data-ttu-id="daafd-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daafd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daafd-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="daafd-119">-IpRule</span></span>
<span data-ttu-id="daafd-120">Conta de serviços cognitiva NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="daafd-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="daafd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="daafd-121">-Name</span></span>
<span data-ttu-id="daafd-122">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="daafd-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="daafd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daafd-123">-ResourceGroupName</span></span>
<span data-ttu-id="daafd-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daafd-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="daafd-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="daafd-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="daafd-126">Conta de serviços cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="daafd-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="daafd-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="daafd-127">-Confirm</span></span>
<span data-ttu-id="daafd-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daafd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daafd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daafd-129">-WhatIf</span></span>
<span data-ttu-id="daafd-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daafd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daafd-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daafd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daafd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daafd-132">CommonParameters</span></span>
<span data-ttu-id="daafd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daafd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daafd-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daafd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daafd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daafd-135">INPUTS</span></span>

### <span data-ttu-id="daafd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="daafd-136">System.String</span></span>

### <span data-ttu-id="daafd-137">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="daafd-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="daafd-138">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="daafd-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="daafd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daafd-139">OUTPUTS</span></span>

### <span data-ttu-id="daafd-140">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daafd-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="daafd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daafd-141">NOTES</span></span>

## <span data-ttu-id="daafd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daafd-142">RELATED LINKS</span></span>
