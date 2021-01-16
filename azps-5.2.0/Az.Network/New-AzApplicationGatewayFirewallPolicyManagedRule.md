---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259417"
---
# <span data-ttu-id="76a62-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="76a62-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="76a62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76a62-102">SYNOPSIS</span></span>
<span data-ttu-id="76a62-103">Crie ManagedRules para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="76a62-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="76a62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76a62-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76a62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76a62-105">DESCRIPTION</span></span>
<span data-ttu-id="76a62-106">O **New-AzApplicationGatewayFirewallPolicyManagedRule** cria regras gerenciadas para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="76a62-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="76a62-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76a62-107">EXAMPLES</span></span>

### <span data-ttu-id="76a62-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76a62-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="76a62-109">O comando cria regras gerenciadas uma lista de ManagedRuleSet com $managedRuleSet e uma lista de exclusão com entradas como $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="76a62-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="76a62-110">OS</span><span class="sxs-lookup"><span data-stu-id="76a62-110">PARAMETERS</span></span>

### <span data-ttu-id="76a62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a62-111">-DefaultProfile</span></span>
<span data-ttu-id="76a62-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76a62-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a62-113">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="76a62-113">-Exclusion</span></span>
<span data-ttu-id="76a62-114">Lista de entradas de exclusão.</span><span class="sxs-lookup"><span data-stu-id="76a62-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a62-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="76a62-115">-ManagedRuleSet</span></span>
<span data-ttu-id="76a62-116">Lista de ruleSets gerenciados.</span><span class="sxs-lookup"><span data-stu-id="76a62-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a62-117">CommonParameters</span></span>
<span data-ttu-id="76a62-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a62-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a62-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a62-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76a62-120">INPUTS</span></span>

### <span data-ttu-id="76a62-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76a62-121">None</span></span>

## <span data-ttu-id="76a62-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76a62-122">OUTPUTS</span></span>

### <span data-ttu-id="76a62-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="76a62-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="76a62-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76a62-124">NOTES</span></span>

## <span data-ttu-id="76a62-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76a62-125">RELATED LINKS</span></span>
