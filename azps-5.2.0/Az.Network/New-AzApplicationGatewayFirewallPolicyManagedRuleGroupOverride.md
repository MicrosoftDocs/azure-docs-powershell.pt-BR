---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260477"
---
# <span data-ttu-id="924c2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="924c2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="924c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="924c2-102">SYNOPSIS</span></span>
<span data-ttu-id="924c2-103">Cria a entrada RuleGroupOverride no ManagedRuleSets para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="924c2-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="924c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="924c2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="924c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="924c2-105">DESCRIPTION</span></span>
<span data-ttu-id="924c2-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** cria uma entrada ruleGroupOverride em um managedRuleSet para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="924c2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="924c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="924c2-107">EXAMPLES</span></span>

### <span data-ttu-id="924c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="924c2-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="924c2-109">Cria uma entrada RuleGroupOverride com o nome do grupo como $ruleName e regras como $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="924c2-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="924c2-110">Atribui o mesmo $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="924c2-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="924c2-111">OS</span><span class="sxs-lookup"><span data-stu-id="924c2-111">PARAMETERS</span></span>

### <span data-ttu-id="924c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924c2-112">-DefaultProfile</span></span>
<span data-ttu-id="924c2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="924c2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="924c2-114">-Regra</span><span class="sxs-lookup"><span data-stu-id="924c2-114">-Rule</span></span>
<span data-ttu-id="924c2-115">Lista de regras.</span><span class="sxs-lookup"><span data-stu-id="924c2-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924c2-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="924c2-116">-RuleGroupName</span></span>
<span data-ttu-id="924c2-117">Especifique o ruleGroupName em uma entrada do meu fio de substituição.</span><span class="sxs-lookup"><span data-stu-id="924c2-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="924c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924c2-118">CommonParameters</span></span>
<span data-ttu-id="924c2-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="924c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924c2-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="924c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924c2-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="924c2-121">INPUTS</span></span>

### <span data-ttu-id="924c2-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="924c2-122">None</span></span>

## <span data-ttu-id="924c2-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="924c2-123">OUTPUTS</span></span>

### <span data-ttu-id="924c2-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="924c2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="924c2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="924c2-125">NOTES</span></span>

## <span data-ttu-id="924c2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="924c2-126">RELATED LINKS</span></span>
