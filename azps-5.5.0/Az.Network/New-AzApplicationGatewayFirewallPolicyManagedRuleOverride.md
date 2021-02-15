---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111650"
---
# <span data-ttu-id="6df24-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6df24-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="6df24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6df24-102">SYNOPSIS</span></span>
<span data-ttu-id="6df24-103">Cria uma entrada managedRuleOverride para a entrada do RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="6df24-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="6df24-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df24-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df24-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6df24-105">DESCRIPTION</span></span>
<span data-ttu-id="6df24-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** cria uma entrada ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="6df24-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="6df24-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6df24-107">EXAMPLES</span></span>

### <span data-ttu-id="6df24-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6df24-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="6df24-109">Cria uma entrada ruleOverride com RuleId como $ruleId e Estado como Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6df24-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="6df24-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df24-110">PARAMETERS</span></span>

### <span data-ttu-id="6df24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df24-111">-DefaultProfile</span></span>
<span data-ttu-id="6df24-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6df24-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df24-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6df24-113">-RuleId</span></span>
<span data-ttu-id="6df24-114">Especifique a RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="6df24-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="6df24-115">-Estado</span><span class="sxs-lookup"><span data-stu-id="6df24-115">-State</span></span>
<span data-ttu-id="6df24-116">Especifique a RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="6df24-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="6df24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df24-117">CommonParameters</span></span>
<span data-ttu-id="6df24-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df24-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6df24-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df24-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="6df24-120">INPUTS</span></span>

### <span data-ttu-id="6df24-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6df24-121">None</span></span>

## <span data-ttu-id="6df24-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="6df24-122">OUTPUTS</span></span>

### <span data-ttu-id="6df24-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6df24-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="6df24-124">Notas</span><span class="sxs-lookup"><span data-stu-id="6df24-124">NOTES</span></span>

## <span data-ttu-id="6df24-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6df24-125">RELATED LINKS</span></span>
