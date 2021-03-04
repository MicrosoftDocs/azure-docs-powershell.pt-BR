---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: d8cb1e6f36433168d830c79c2bcbf8b5c259cf32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886722"
---
# <span data-ttu-id="add85-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="add85-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="add85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add85-102">SYNOPSIS</span></span>
<span data-ttu-id="add85-103">Cria um ManagedRuleSet para firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="add85-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="add85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="add85-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add85-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="add85-105">DESCRIPTION</span></span>
<span data-ttu-id="add85-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** cria uma regra gerenciada para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="add85-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="add85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="add85-107">EXAMPLES</span></span>

### <span data-ttu-id="add85-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="add85-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="add85-109">Cria um ManagedRuleSet com ruleSetType como $ruleSetType, ruleSetVersion como $ruleSetVersion e RuleGroupOverrides como uma lista com inteiros como $ruleGroupOverride 1, $ruleGroupOverride 2 O novo ManagedRuleSet é atribuído ao $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="add85-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="add85-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="add85-110">PARAMETERS</span></span>

### <span data-ttu-id="add85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add85-111">-DefaultProfile</span></span>
<span data-ttu-id="add85-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="add85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add85-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="add85-113">-RuleGroupOverride</span></span>
<span data-ttu-id="add85-114">Substituições de grupo de regras.</span><span class="sxs-lookup"><span data-stu-id="add85-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add85-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="add85-115">-RuleSetType</span></span>
<span data-ttu-id="add85-116">Especificar RuleSetType em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="add85-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="add85-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="add85-117">-RuleSetVersion</span></span>
<span data-ttu-id="add85-118">Especificar RuleSetVersion em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="add85-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="add85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add85-119">CommonParameters</span></span>
<span data-ttu-id="add85-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add85-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="add85-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add85-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="add85-122">INPUTS</span></span>

### <span data-ttu-id="add85-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="add85-123">None</span></span>

## <span data-ttu-id="add85-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="add85-124">OUTPUTS</span></span>

### <span data-ttu-id="add85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="add85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="add85-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="add85-126">NOTES</span></span>

## <span data-ttu-id="add85-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="add85-127">RELATED LINKS</span></span>
