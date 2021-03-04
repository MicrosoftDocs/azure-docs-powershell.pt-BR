---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 934c69071e90ebb1a38bf4e1fda5e631364ab87b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892085"
---
# <span data-ttu-id="f8e72-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f8e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e72-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e72-103">Modifica um conjunto de regras de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8e72-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="f8e72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f8e72-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e72-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f8e72-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e72-106">O cmdlet **Set-AzApplicationGatewayRewriteRuleSet** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="f8e72-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f8e72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8e72-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e72-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8e72-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="f8e72-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f8e72-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f8e72-110">O segundo comando modifica o conjunto de regras de regra de regra de reescrita para o gateway de aplicativo usar regras de reescrita especificadas na variável $rule de reescrita.</span><span class="sxs-lookup"><span data-stu-id="f8e72-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="f8e72-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f8e72-111">PARAMETERS</span></span>

### <span data-ttu-id="f8e72-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8e72-112">-ApplicationGateway</span></span>
<span data-ttu-id="f8e72-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8e72-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e72-114">-DefaultProfile</span></span>
<span data-ttu-id="f8e72-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8e72-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f8e72-116">-Name</span></span>
<span data-ttu-id="f8e72-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="f8e72-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="f8e72-118">-RewriteRule</span></span>
<span data-ttu-id="f8e72-119">Lista de regras de regravar</span><span class="sxs-lookup"><span data-stu-id="f8e72-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="f8e72-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e72-120">CommonParameters</span></span>
<span data-ttu-id="f8e72-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e72-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e72-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e72-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e72-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8e72-123">INPUTS</span></span>

### <span data-ttu-id="f8e72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8e72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f8e72-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f8e72-125">OUTPUTS</span></span>

### <span data-ttu-id="f8e72-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8e72-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f8e72-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="f8e72-127">NOTES</span></span>

## <span data-ttu-id="f8e72-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8e72-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8e72-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f8e72-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f8e72-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f8e72-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f8e72-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f8e72-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f8e72-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f8e72-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f8e72-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8e72-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
