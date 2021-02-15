---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117408"
---
# <span data-ttu-id="6aa34-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6aa34-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="6aa34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6aa34-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa34-103">Cria uma regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6aa34-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="6aa34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6aa34-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa34-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aa34-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa34-106">O cmdlet **New-AzApplicationGatewayRewriteRule** cria uma regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa34-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="6aa34-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6aa34-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa34-108">Exemplo 1: Criar uma regra de reescrita para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6aa34-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="6aa34-109">Esse comando cria uma regra de reescrita chamada regra1 e armazena o resultado na variável chamada $rule.</span><span class="sxs-lookup"><span data-stu-id="6aa34-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="6aa34-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aa34-110">PARAMETERS</span></span>

### <span data-ttu-id="6aa34-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-111">-ActionSet</span></span>
<span data-ttu-id="6aa34-112">ActionSet da regra de reescrita</span><span class="sxs-lookup"><span data-stu-id="6aa34-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="6aa34-113">-Condição</span><span class="sxs-lookup"><span data-stu-id="6aa34-113">-Condition</span></span>
<span data-ttu-id="6aa34-114">Condição para que a regra de reescrita seja executada</span><span class="sxs-lookup"><span data-stu-id="6aa34-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="6aa34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa34-115">-DefaultProfile</span></span>
<span data-ttu-id="6aa34-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa34-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6aa34-117">-Name</span></span>
<span data-ttu-id="6aa34-118">O nome da Regra Reescrita</span><span class="sxs-lookup"><span data-stu-id="6aa34-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="6aa34-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="6aa34-119">-RuleSequence</span></span>
<span data-ttu-id="6aa34-120">A ordem das regras desta regra de reescrita no conjunto de regras de reescrita</span><span class="sxs-lookup"><span data-stu-id="6aa34-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="6aa34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa34-121">CommonParameters</span></span>
<span data-ttu-id="6aa34-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa34-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa34-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa34-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="6aa34-124">INPUTS</span></span>

### <span data-ttu-id="6aa34-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6aa34-125">None</span></span>

## <span data-ttu-id="6aa34-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="6aa34-126">OUTPUTS</span></span>

### <span data-ttu-id="6aa34-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6aa34-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="6aa34-128">Notas</span><span class="sxs-lookup"><span data-stu-id="6aa34-128">NOTES</span></span>

## <span data-ttu-id="6aa34-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6aa34-129">RELATED LINKS</span></span>

[<span data-ttu-id="6aa34-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6aa34-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6aa34-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6aa34-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6aa34-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6aa34-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6aa34-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="6aa34-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aa34-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
