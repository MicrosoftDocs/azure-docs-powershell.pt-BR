---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888235"
---
# <span data-ttu-id="8fe29-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8fe29-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="8fe29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe29-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe29-103">Cria uma exclusão na Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="8fe29-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="8fe29-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8fe29-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe29-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8fe29-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe29-106">O cmdlet **New-AzApplicationGatewayFirewallPolicyExclusion** uma nova lista de regras de exclusão para política de firewall.</span><span class="sxs-lookup"><span data-stu-id="8fe29-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="8fe29-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fe29-107">EXAMPLES</span></span>

### <span data-ttu-id="8fe29-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fe29-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="8fe29-109">Este comando cria uma nova entrada de exclusão para a variável denominada RequestHeaderNames e um operador chamado StartsWith e Seletor denominado xyz.</span><span class="sxs-lookup"><span data-stu-id="8fe29-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="8fe29-110">A entrada de exclusão é salva $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="8fe29-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="8fe29-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8fe29-111">PARAMETERS</span></span>

### <span data-ttu-id="8fe29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe29-112">-DefaultProfile</span></span>
<span data-ttu-id="8fe29-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fe29-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="8fe29-114">-MatchVariable</span></span>
<span data-ttu-id="8fe29-115">A variável a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8fe29-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe29-116">-Seletor</span><span class="sxs-lookup"><span data-stu-id="8fe29-116">-Selector</span></span>
<span data-ttu-id="8fe29-117">Quando variável é uma coleção, o operador usado para especificar a quais elementos na coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="8fe29-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="8fe29-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="8fe29-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="8fe29-119">Quando variável for uma coleção, opere no seletor para especificar a quais elementos na coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="8fe29-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe29-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe29-120">CommonParameters</span></span>
<span data-ttu-id="8fe29-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe29-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe29-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fe29-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe29-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fe29-123">INPUTS</span></span>

### <span data-ttu-id="8fe29-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8fe29-124">None</span></span>

## <span data-ttu-id="8fe29-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8fe29-125">OUTPUTS</span></span>

### <span data-ttu-id="8fe29-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8fe29-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="8fe29-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="8fe29-127">NOTES</span></span>

## <span data-ttu-id="8fe29-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fe29-128">RELATED LINKS</span></span>
