---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890614"
---
# <span data-ttu-id="e7be8-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e7be8-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="e7be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e7be8-103">Cria uma entrada managedRuleOverride para entrada RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="e7be8-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="e7be8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7be8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7be8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7be8-105">DESCRIPTION</span></span>
<span data-ttu-id="e7be8-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** cria uma entrada ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="e7be8-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="e7be8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7be8-107">EXAMPLES</span></span>

### <span data-ttu-id="e7be8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7be8-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="e7be8-109">Cria uma entrada ruleOverride com RuleId como $ruleId e Estado como Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e7be8-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="e7be8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7be8-110">PARAMETERS</span></span>

### <span data-ttu-id="e7be8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7be8-111">-DefaultProfile</span></span>
<span data-ttu-id="e7be8-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7be8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7be8-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="e7be8-113">-RuleId</span></span>
<span data-ttu-id="e7be8-114">Especifique o RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="e7be8-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="e7be8-115">-State</span><span class="sxs-lookup"><span data-stu-id="e7be8-115">-State</span></span>
<span data-ttu-id="e7be8-116">Especifique o RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="e7be8-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7be8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7be8-117">CommonParameters</span></span>
<span data-ttu-id="e7be8-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7be8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7be8-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7be8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7be8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7be8-120">INPUTS</span></span>

### <span data-ttu-id="e7be8-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e7be8-121">None</span></span>

## <span data-ttu-id="e7be8-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7be8-122">OUTPUTS</span></span>

### <span data-ttu-id="e7be8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e7be8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="e7be8-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7be8-124">NOTES</span></span>

## <span data-ttu-id="e7be8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7be8-125">RELATED LINKS</span></span>
