---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259418"
---
# <span data-ttu-id="02827-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="02827-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="02827-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02827-102">SYNOPSIS</span></span>
<span data-ttu-id="02827-103">Cria uma exclusão na política de firewall</span><span class="sxs-lookup"><span data-stu-id="02827-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="02827-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02827-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02827-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02827-105">DESCRIPTION</span></span>
<span data-ttu-id="02827-106">O cmdlet **New-AzApplicationGatewayFirewallPolicyExclusion** é uma nova lista de regras de exclusão para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="02827-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="02827-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02827-107">EXAMPLES</span></span>

### <span data-ttu-id="02827-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02827-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="02827-109">Esse comando cria uma nova entrada de exclusão para a variável chamada RequestHeaderNames e o operador chamado StartsWith e selector chamado XYZ.</span><span class="sxs-lookup"><span data-stu-id="02827-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="02827-110">A entrada de exclusão é salva em $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="02827-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="02827-111">OS</span><span class="sxs-lookup"><span data-stu-id="02827-111">PARAMETERS</span></span>

### <span data-ttu-id="02827-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02827-112">-DefaultProfile</span></span>
<span data-ttu-id="02827-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02827-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02827-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="02827-114">-MatchVariable</span></span>
<span data-ttu-id="02827-115">A variável a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="02827-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="02827-116">-Seletor</span><span class="sxs-lookup"><span data-stu-id="02827-116">-Selector</span></span>
<span data-ttu-id="02827-117">Quando Variable é uma coleção, operador usado para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="02827-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="02827-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="02827-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="02827-119">Quando variável é uma coleção, opere no seletor para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="02827-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="02827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02827-120">CommonParameters</span></span>
<span data-ttu-id="02827-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02827-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02827-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02827-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02827-123">INPUTS</span></span>

### <span data-ttu-id="02827-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02827-124">None</span></span>

## <span data-ttu-id="02827-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02827-125">OUTPUTS</span></span>

### <span data-ttu-id="02827-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="02827-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="02827-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02827-127">NOTES</span></span>

## <span data-ttu-id="02827-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02827-128">RELATED LINKS</span></span>
