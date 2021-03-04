---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893139"
---
# <span data-ttu-id="308eb-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="308eb-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="308eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308eb-102">SYNOPSIS</span></span>
<span data-ttu-id="308eb-103">Cria uma regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="308eb-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="308eb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="308eb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="308eb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="308eb-105">DESCRIPTION</span></span>
<span data-ttu-id="308eb-106">O cmdlet **New-AzApplicationGatewayRewriteRule** cria uma regra de regra de regra para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="308eb-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="308eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="308eb-107">EXAMPLES</span></span>

### <span data-ttu-id="308eb-108">Exemplo 1 : Criar uma regra de regra para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="308eb-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="308eb-109">Este comando cria uma regra de regra1 e armazena o resultado na variável chamada $rule.</span><span class="sxs-lookup"><span data-stu-id="308eb-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="308eb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="308eb-110">PARAMETERS</span></span>

### <span data-ttu-id="308eb-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="308eb-111">-ActionSet</span></span>
<span data-ttu-id="308eb-112">ActionSet da regra de reescrita</span><span class="sxs-lookup"><span data-stu-id="308eb-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="308eb-113">-Condition</span></span>
<span data-ttu-id="308eb-114">Condição para a regra de reescrita ser executada</span><span class="sxs-lookup"><span data-stu-id="308eb-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308eb-115">-DefaultProfile</span></span>
<span data-ttu-id="308eb-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="308eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308eb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="308eb-117">-Name</span></span>
<span data-ttu-id="308eb-118">O nome do ReescritaRule</span><span class="sxs-lookup"><span data-stu-id="308eb-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="308eb-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="308eb-119">-RuleSequence</span></span>
<span data-ttu-id="308eb-120">A ordem de regra dessa regra de regra de reescrita no conjunto de regras de regra de reescrita</span><span class="sxs-lookup"><span data-stu-id="308eb-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308eb-121">CommonParameters</span></span>
<span data-ttu-id="308eb-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308eb-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308eb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308eb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="308eb-124">INPUTS</span></span>

### <span data-ttu-id="308eb-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="308eb-125">None</span></span>

## <span data-ttu-id="308eb-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="308eb-126">OUTPUTS</span></span>

### <span data-ttu-id="308eb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="308eb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="308eb-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="308eb-128">NOTES</span></span>

## <span data-ttu-id="308eb-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="308eb-129">RELATED LINKS</span></span>

[<span data-ttu-id="308eb-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="308eb-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="308eb-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="308eb-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="308eb-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="308eb-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="308eb-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="308eb-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="308eb-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="308eb-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="308eb-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="308eb-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="308eb-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="308eb-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
