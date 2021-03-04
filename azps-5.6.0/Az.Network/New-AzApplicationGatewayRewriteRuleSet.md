---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 8bd540c30551451bd729126c35c4d778c700591f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891792"
---
# <span data-ttu-id="978e9-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="978e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978e9-102">SYNOPSIS</span></span>
<span data-ttu-id="978e9-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="978e9-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="978e9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="978e9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="978e9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="978e9-105">DESCRIPTION</span></span>
<span data-ttu-id="978e9-106">O cmdlet **New-AzApplicationGatewayRewriteRuleSet** cria um conjunto de regras de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="978e9-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="978e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="978e9-107">EXAMPLES</span></span>

### <span data-ttu-id="978e9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="978e9-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="978e9-109">Este comando cria um conjunto de regras de regra de reescrita denominado ruleset1 e armazena o resultado na variável chamada $ruleset.</span><span class="sxs-lookup"><span data-stu-id="978e9-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="978e9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="978e9-110">PARAMETERS</span></span>

### <span data-ttu-id="978e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978e9-111">-DefaultProfile</span></span>
<span data-ttu-id="978e9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="978e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978e9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="978e9-113">-Name</span></span>
<span data-ttu-id="978e9-114">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="978e9-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="978e9-115">-RewriteRule</span></span>
<span data-ttu-id="978e9-116">Lista de regras de regravar</span><span class="sxs-lookup"><span data-stu-id="978e9-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978e9-117">CommonParameters</span></span>
<span data-ttu-id="978e9-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978e9-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="978e9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978e9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="978e9-120">INPUTS</span></span>

### <span data-ttu-id="978e9-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="978e9-121">None</span></span>

## <span data-ttu-id="978e9-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="978e9-122">OUTPUTS</span></span>

### <span data-ttu-id="978e9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="978e9-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="978e9-124">NOTES</span></span>

## <span data-ttu-id="978e9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="978e9-125">RELATED LINKS</span></span>

[<span data-ttu-id="978e9-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="978e9-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="978e9-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="978e9-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="978e9-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="978e9-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="978e9-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="978e9-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="978e9-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="978e9-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="978e9-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
