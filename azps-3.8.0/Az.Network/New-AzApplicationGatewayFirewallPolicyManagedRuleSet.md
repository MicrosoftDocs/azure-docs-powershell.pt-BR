---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944812"
---
# <span data-ttu-id="f1692-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1692-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="f1692-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1692-102">SYNOPSIS</span></span>
<span data-ttu-id="f1692-103">Cria um ManagedRuleSet para o firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f1692-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="f1692-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1692-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1692-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1692-105">DESCRIPTION</span></span>
<span data-ttu-id="f1692-106">O **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** cria regras gerenciadas para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="f1692-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="f1692-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1692-107">EXAMPLES</span></span>

### <span data-ttu-id="f1692-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1692-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="f1692-109">Cria um ManagedRuleSet com ruleSettype como $ruleSetType, ruleSetVersion como $ruleSetVersion e RuleGroupOverrides como uma lista de inteiros como $ruleGroupOverride 1, $ruleGroupOverride 2 que o novo ManagedRuleSet está atribuído a $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1692-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="f1692-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1692-110">PARAMETERS</span></span>

### <span data-ttu-id="f1692-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1692-111">-DefaultProfile</span></span>
<span data-ttu-id="f1692-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1692-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1692-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f1692-113">-RuleGroupOverride</span></span>
<span data-ttu-id="f1692-114">Substituições de grupo de regra.</span><span class="sxs-lookup"><span data-stu-id="f1692-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="f1692-115">-RuleSettype</span><span class="sxs-lookup"><span data-stu-id="f1692-115">-RuleSetType</span></span>
<span data-ttu-id="f1692-116">Especificar o RuleSettype em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1692-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="f1692-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f1692-117">-RuleSetVersion</span></span>
<span data-ttu-id="f1692-118">Especificar o RuleSetVersion em um managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1692-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="f1692-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1692-119">CommonParameters</span></span>
<span data-ttu-id="f1692-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1692-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1692-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1692-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1692-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1692-122">INPUTS</span></span>

### <span data-ttu-id="f1692-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f1692-123">None</span></span>

## <span data-ttu-id="f1692-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1692-124">OUTPUTS</span></span>

### <span data-ttu-id="f1692-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1692-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="f1692-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1692-126">NOTES</span></span>

## <span data-ttu-id="f1692-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1692-127">RELATED LINKS</span></span>
