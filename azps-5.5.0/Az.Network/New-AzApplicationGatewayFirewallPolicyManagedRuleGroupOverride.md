---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111654"
---
# <span data-ttu-id="61ec3-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="61ec3-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="61ec3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="61ec3-103">Cria a entrada RuleGroupOverride em ManagedRuleSets para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="61ec3-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="61ec3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61ec3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ec3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="61ec3-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** cria uma entrada ruleGroupOverride em um managedRuleSet para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="61ec3-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="61ec3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="61ec3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61ec3-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="61ec3-109">Cria uma entrada RuleGroupOverride com nome de grupo como $ruleName e Regras como $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="61ec3-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="61ec3-110">Atribui o mesmo ao $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="61ec3-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="61ec3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61ec3-111">PARAMETERS</span></span>

### <span data-ttu-id="61ec3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ec3-112">-DefaultProfile</span></span>
<span data-ttu-id="61ec3-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61ec3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ec3-114">-Regra</span><span class="sxs-lookup"><span data-stu-id="61ec3-114">-Rule</span></span>
<span data-ttu-id="61ec3-115">Lista de Regras.</span><span class="sxs-lookup"><span data-stu-id="61ec3-115">List of Rules.</span></span>

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

### <span data-ttu-id="61ec3-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="61ec3-116">-RuleGroupName</span></span>
<span data-ttu-id="61ec3-117">Especifique o ruleGroupName em uma entrada substituir RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="61ec3-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="61ec3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ec3-118">CommonParameters</span></span>
<span data-ttu-id="61ec3-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ec3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ec3-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61ec3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ec3-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="61ec3-121">INPUTS</span></span>

### <span data-ttu-id="61ec3-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61ec3-122">None</span></span>

## <span data-ttu-id="61ec3-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="61ec3-123">OUTPUTS</span></span>

### <span data-ttu-id="61ec3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="61ec3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="61ec3-125">Notas</span><span class="sxs-lookup"><span data-stu-id="61ec3-125">NOTES</span></span>

## <span data-ttu-id="61ec3-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61ec3-126">RELATED LINKS</span></span>
