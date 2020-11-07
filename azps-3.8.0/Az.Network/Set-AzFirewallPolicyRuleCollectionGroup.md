---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942509"
---
# <span data-ttu-id="d193a-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d193a-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d193a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d193a-102">SYNOPSIS</span></span>
<span data-ttu-id="d193a-103">salva um grupo da coleção de regras de firewall do Azure modificada</span><span class="sxs-lookup"><span data-stu-id="d193a-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="d193a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d193a-104">SYNTAX</span></span>

### <span data-ttu-id="d193a-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d193a-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d193a-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d193a-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d193a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d193a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d193a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d193a-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d193a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d193a-109">DESCRIPTION</span></span>
<span data-ttu-id="d193a-110">O cmdlet **set-AzFirewallPolicyRuleCollectionGroup** atualiza um grupo de conjuntos de regras em uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="d193a-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d193a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d193a-111">EXAMPLES</span></span>

### <span data-ttu-id="d193a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d193a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="d193a-113">Este exemplo atualiza um grupo de coleção de regras na política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="d193a-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="d193a-114">OS</span><span class="sxs-lookup"><span data-stu-id="d193a-114">PARAMETERS</span></span>

### <span data-ttu-id="d193a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d193a-115">-DefaultProfile</span></span>
<span data-ttu-id="d193a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d193a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d193a-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="d193a-117">-FirewallPolicyName</span></span>
<span data-ttu-id="d193a-118">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="d193a-118">The name of the firewall policy</span></span>

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

### <span data-ttu-id="d193a-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d193a-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="d193a-120">Política de firewall.</span><span class="sxs-lookup"><span data-stu-id="d193a-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d193a-121">-InputObject</span></span>
<span data-ttu-id="d193a-122">A lista de regras</span><span class="sxs-lookup"><span data-stu-id="d193a-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d193a-123">-Name</span></span>
<span data-ttu-id="d193a-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d193a-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-125">-Priority</span><span class="sxs-lookup"><span data-stu-id="d193a-125">-Priority</span></span>
<span data-ttu-id="d193a-126">A prioridade do grupo de regras</span><span class="sxs-lookup"><span data-stu-id="d193a-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d193a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d193a-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d193a-128">The resource group name.</span></span>

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

### <span data-ttu-id="d193a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d193a-129">-ResourceId</span></span>
<span data-ttu-id="d193a-130">A ID do recurso do agrupamento da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="d193a-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="d193a-131">-RuleCollection</span></span>
<span data-ttu-id="d193a-132">A lista de coleções de regras</span><span class="sxs-lookup"><span data-stu-id="d193a-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d193a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d193a-133">-Confirm</span></span>
<span data-ttu-id="d193a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d193a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d193a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d193a-135">-WhatIf</span></span>
<span data-ttu-id="d193a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d193a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d193a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d193a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d193a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d193a-138">CommonParameters</span></span>
<span data-ttu-id="d193a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d193a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d193a-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d193a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d193a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d193a-141">INPUTS</span></span>

### <span data-ttu-id="d193a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d193a-142">System.String</span></span>

### <span data-ttu-id="d193a-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d193a-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="d193a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d193a-144">OUTPUTS</span></span>

### <span data-ttu-id="d193a-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d193a-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d193a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d193a-146">NOTES</span></span>

## <span data-ttu-id="d193a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d193a-147">RELATED LINKS</span></span>
