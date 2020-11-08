---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124513"
---
# <span data-ttu-id="438bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="438bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="438bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="438bc-102">SYNOPSIS</span></span>
<span data-ttu-id="438bc-103">Cria uma entrada managedRuleOverride para a entrada RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="438bc-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="438bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="438bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="438bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="438bc-105">DESCRIPTION</span></span>
<span data-ttu-id="438bc-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** cria uma entrada ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="438bc-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="438bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="438bc-107">EXAMPLES</span></span>

### <span data-ttu-id="438bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="438bc-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="438bc-109">Cria uma entrada ruleOverride com RuleId como $ruleId e estado como Disabled.</span><span class="sxs-lookup"><span data-stu-id="438bc-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="438bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="438bc-110">PARAMETERS</span></span>

### <span data-ttu-id="438bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438bc-111">-DefaultProfile</span></span>
<span data-ttu-id="438bc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="438bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="438bc-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="438bc-113">-RuleId</span></span>
<span data-ttu-id="438bc-114">Especifique a RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="438bc-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="438bc-115">-Estado</span><span class="sxs-lookup"><span data-stu-id="438bc-115">-State</span></span>
<span data-ttu-id="438bc-116">Especifique a RuleId na entrada de regra de substituição.</span><span class="sxs-lookup"><span data-stu-id="438bc-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="438bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438bc-117">CommonParameters</span></span>
<span data-ttu-id="438bc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438bc-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="438bc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438bc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="438bc-120">INPUTS</span></span>

### <span data-ttu-id="438bc-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="438bc-121">None</span></span>

## <span data-ttu-id="438bc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="438bc-122">OUTPUTS</span></span>

### <span data-ttu-id="438bc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="438bc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="438bc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="438bc-124">NOTES</span></span>

## <span data-ttu-id="438bc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="438bc-125">RELATED LINKS</span></span>
