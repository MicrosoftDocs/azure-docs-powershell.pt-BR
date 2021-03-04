---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891797"
---
# <span data-ttu-id="9c104-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="9c104-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="9c104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c104-102">SYNOPSIS</span></span>
<span data-ttu-id="9c104-103">Cria a entrada RuleGroupOverride em ManagedRuleSets para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="9c104-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="9c104-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c104-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c104-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c104-105">DESCRIPTION</span></span>
<span data-ttu-id="9c104-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** cria uma entrada ruleGroupOverride em um managedRuleSet para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="9c104-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="9c104-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c104-107">EXAMPLES</span></span>

### <span data-ttu-id="9c104-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c104-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="9c104-109">Cria uma entrada RuleGroupOverride com nome de grupo como $ruleName e Regras como $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="9c104-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="9c104-110">Atribui o mesmo a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="9c104-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="9c104-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c104-111">PARAMETERS</span></span>

### <span data-ttu-id="9c104-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c104-112">-DefaultProfile</span></span>
<span data-ttu-id="9c104-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c104-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c104-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="9c104-114">-Rule</span></span>
<span data-ttu-id="9c104-115">Lista de regras.</span><span class="sxs-lookup"><span data-stu-id="9c104-115">List of Rules.</span></span>

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

### <span data-ttu-id="9c104-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="9c104-116">-RuleGroupName</span></span>
<span data-ttu-id="9c104-117">Especifique o ruleGroupName em uma entrada substituir RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="9c104-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="9c104-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c104-118">CommonParameters</span></span>
<span data-ttu-id="9c104-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c104-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c104-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c104-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c104-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c104-121">INPUTS</span></span>

### <span data-ttu-id="9c104-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9c104-122">None</span></span>

## <span data-ttu-id="9c104-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c104-123">OUTPUTS</span></span>

### <span data-ttu-id="9c104-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="9c104-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="9c104-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c104-125">NOTES</span></span>

## <span data-ttu-id="9c104-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c104-126">RELATED LINKS</span></span>
