---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: d657c769a32d7c042a12a56571343885c526eea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889198"
---
# <span data-ttu-id="73f34-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="73f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f34-102">SYNOPSIS</span></span>
<span data-ttu-id="73f34-103">Adiciona uma regra de regra de reescrita definida a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73f34-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="73f34-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73f34-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73f34-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73f34-105">DESCRIPTION</span></span>
<span data-ttu-id="73f34-106">O cmdlet **Add-AzApplicationGatewayRewriteRuleSet** adiciona uma regra de reescrita definida a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73f34-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="73f34-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73f34-107">EXAMPLES</span></span>

### <span data-ttu-id="73f34-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73f34-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="73f34-109">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="73f34-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="73f34-110">O segundo comando adiciona a regra de regra de reescrita definida ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73f34-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="73f34-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73f34-111">PARAMETERS</span></span>

### <span data-ttu-id="73f34-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f34-112">-ApplicationGateway</span></span>
<span data-ttu-id="73f34-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f34-113">The applicationGateway</span></span>

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

### <span data-ttu-id="73f34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f34-114">-DefaultProfile</span></span>
<span data-ttu-id="73f34-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73f34-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f34-116">-Name</span><span class="sxs-lookup"><span data-stu-id="73f34-116">-Name</span></span>
<span data-ttu-id="73f34-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="73f34-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="73f34-118">-RewriteRule</span></span>
<span data-ttu-id="73f34-119">Lista de regras de regravar</span><span class="sxs-lookup"><span data-stu-id="73f34-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="73f34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f34-120">CommonParameters</span></span>
<span data-ttu-id="73f34-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f34-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f34-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f34-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73f34-123">INPUTS</span></span>

### <span data-ttu-id="73f34-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f34-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73f34-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73f34-125">OUTPUTS</span></span>

### <span data-ttu-id="73f34-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f34-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73f34-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="73f34-127">NOTES</span></span>

## <span data-ttu-id="73f34-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73f34-128">RELATED LINKS</span></span>

[<span data-ttu-id="73f34-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="73f34-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="73f34-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="73f34-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f34-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="73f34-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="73f34-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="73f34-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73f34-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="73f34-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f34-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
