---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941812"
---
# <span data-ttu-id="40c7f-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="40c7f-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="40c7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="40c7f-103">Criar um novo grupo de coleção de regras de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="40c7f-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="40c7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40c7f-104">SYNTAX</span></span>

### <span data-ttu-id="40c7f-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c7f-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40c7f-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c7f-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40c7f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40c7f-107">DESCRIPTION</span></span>
<span data-ttu-id="40c7f-108">O cmdlet **New-AzFirewallPolicyRuleCollectionGroup** cria um grupo de coleção de regras em uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="40c7f-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="40c7f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40c7f-109">EXAMPLES</span></span>

### <span data-ttu-id="40c7f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40c7f-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="40c7f-111">Este exemplo cria um grupo de coleção de regras na política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="40c7f-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="40c7f-112">OS</span><span class="sxs-lookup"><span data-stu-id="40c7f-112">PARAMETERS</span></span>

### <span data-ttu-id="40c7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c7f-113">-DefaultProfile</span></span>
<span data-ttu-id="40c7f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40c7f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c7f-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="40c7f-115">-FirewallPolicyName</span></span>
<span data-ttu-id="40c7f-116">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="40c7f-116">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c7f-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="40c7f-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="40c7f-118">Política de firewall.</span><span class="sxs-lookup"><span data-stu-id="40c7f-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c7f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="40c7f-119">-Name</span></span>
<span data-ttu-id="40c7f-120">O nome do grupo de regras</span><span class="sxs-lookup"><span data-stu-id="40c7f-120">The name of the Rule Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c7f-121">-Priority</span><span class="sxs-lookup"><span data-stu-id="40c7f-121">-Priority</span></span>
<span data-ttu-id="40c7f-122">A prioridade do grupo de regras</span><span class="sxs-lookup"><span data-stu-id="40c7f-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="40c7f-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40c7f-124">The resource group name.</span></span>

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

### <span data-ttu-id="40c7f-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="40c7f-125">-RuleCollection</span></span>
<span data-ttu-id="40c7f-126">A lista de regras</span><span class="sxs-lookup"><span data-stu-id="40c7f-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c7f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40c7f-127">-Confirm</span></span>
<span data-ttu-id="40c7f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40c7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c7f-129">-WhatIf</span></span>
<span data-ttu-id="40c7f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c7f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40c7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c7f-132">CommonParameters</span></span>
<span data-ttu-id="40c7f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c7f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40c7f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c7f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40c7f-135">INPUTS</span></span>

### <span data-ttu-id="40c7f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="40c7f-136">System.String</span></span>

### <span data-ttu-id="40c7f-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="40c7f-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="40c7f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40c7f-138">OUTPUTS</span></span>

### <span data-ttu-id="40c7f-139">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="40c7f-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="40c7f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40c7f-140">NOTES</span></span>

## <span data-ttu-id="40c7f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40c7f-141">RELATED LINKS</span></span>
