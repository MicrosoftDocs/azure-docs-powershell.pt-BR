---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944789"
---
# <span data-ttu-id="d7893-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d7893-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="d7893-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7893-102">SYNOPSIS</span></span>
<span data-ttu-id="d7893-103">Cria uma regra de regravação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7893-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="d7893-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7893-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7893-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7893-105">DESCRIPTION</span></span>
<span data-ttu-id="d7893-106">**O cmdlet New-AzApplicationGatewayRewriteRule** cria uma regra de regravação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7893-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="d7893-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7893-107">EXAMPLES</span></span>

### <span data-ttu-id="d7893-108">Exemplo 1: criar uma regra de regravação para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d7893-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="d7893-109">Esse comando cria uma regra de regravação chamada rule1 e armazena o resultado na variável chamada $rule.</span><span class="sxs-lookup"><span data-stu-id="d7893-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="d7893-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7893-110">PARAMETERS</span></span>

### <span data-ttu-id="d7893-111">-Actionset</span><span class="sxs-lookup"><span data-stu-id="d7893-111">-ActionSet</span></span>
<span data-ttu-id="d7893-112">Açãoset da regra de regravação</span><span class="sxs-lookup"><span data-stu-id="d7893-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="d7893-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="d7893-113">-Condition</span></span>
<span data-ttu-id="d7893-114">Condição da regra de regravação a ser executada</span><span class="sxs-lookup"><span data-stu-id="d7893-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="d7893-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7893-115">-DefaultProfile</span></span>
<span data-ttu-id="d7893-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7893-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7893-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7893-117">-Name</span></span>
<span data-ttu-id="d7893-118">O nome do RewriteRule</span><span class="sxs-lookup"><span data-stu-id="d7893-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="d7893-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="d7893-119">-RuleSequence</span></span>
<span data-ttu-id="d7893-120">A classificação de regra desta regra de regravação no conjunto de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="d7893-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="d7893-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7893-121">CommonParameters</span></span>
<span data-ttu-id="d7893-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7893-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7893-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7893-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7893-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7893-124">INPUTS</span></span>

### <span data-ttu-id="d7893-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7893-125">None</span></span>

## <span data-ttu-id="d7893-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7893-126">OUTPUTS</span></span>

### <span data-ttu-id="d7893-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d7893-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="d7893-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7893-128">NOTES</span></span>

## <span data-ttu-id="d7893-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7893-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7893-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7893-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d7893-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7893-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d7893-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7893-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d7893-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7893-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d7893-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7893-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d7893-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d7893-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d7893-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7893-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
