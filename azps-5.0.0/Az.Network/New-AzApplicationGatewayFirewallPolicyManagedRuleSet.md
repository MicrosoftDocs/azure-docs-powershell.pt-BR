---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125625"
---
# <span data-ttu-id="13730-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13730-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="13730-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13730-102">SYNOPSIS</span></span>
<span data-ttu-id="13730-103">Cria um ManagedRuleSet para o firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="13730-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="13730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13730-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13730-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13730-105">DESCRIPTION</span></span>
<span data-ttu-id="13730-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** cria regras gerenciadas para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="13730-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="13730-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13730-107">EXAMPLES</span></span>

### <span data-ttu-id="13730-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13730-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="13730-109">Cria um ManagedRuleSet com ruleSettype como $ruleSetType, ruleSetVersion como $ruleSetVersion e RuleGroupOverrides como uma lista de inteiros como $ruleGroupOverride 1, $ruleGroupOverride 2 que o novo ManagedRuleSet está atribuído a $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13730-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="13730-110">OS</span><span class="sxs-lookup"><span data-stu-id="13730-110">PARAMETERS</span></span>

### <span data-ttu-id="13730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13730-111">-DefaultProfile</span></span>
<span data-ttu-id="13730-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13730-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="13730-113">-RuleGroupOverride</span></span>
<span data-ttu-id="13730-114">Substituições de grupo de regra.</span><span class="sxs-lookup"><span data-stu-id="13730-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="13730-115">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="13730-115">-RuleSetType</span></span>
<span data-ttu-id="13730-116">Especificar o RuleSettype em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13730-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="13730-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="13730-117">-RuleSetVersion</span></span>
<span data-ttu-id="13730-118">Especificar o RuleSetVersion em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13730-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="13730-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13730-119">CommonParameters</span></span>
<span data-ttu-id="13730-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13730-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13730-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13730-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13730-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13730-122">INPUTS</span></span>

### <span data-ttu-id="13730-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="13730-123">None</span></span>

## <span data-ttu-id="13730-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13730-124">OUTPUTS</span></span>

### <span data-ttu-id="13730-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="13730-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="13730-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13730-126">NOTES</span></span>

## <span data-ttu-id="13730-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13730-127">RELATED LINKS</span></span>
