---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263047"
---
# <span data-ttu-id="9c2bb-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9c2bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2bb-103">Adiciona um conjunto de regras de regravação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9c2bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c2bb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c2bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c2bb-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2bb-106">O cmdlet **Add-AzApplicationGatewayRewriteRuleSet** adiciona uma regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9c2bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c2bb-107">EXAMPLES</span></span>

### <span data-ttu-id="9c2bb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c2bb-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="9c2bb-109">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9c2bb-110">O segundo comando adiciona o conjunto de regras de regravação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="9c2bb-111">OS</span><span class="sxs-lookup"><span data-stu-id="9c2bb-111">PARAMETERS</span></span>

### <span data-ttu-id="9c2bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c2bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="9c2bb-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c2bb-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9c2bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2bb-114">-DefaultProfile</span></span>
<span data-ttu-id="9c2bb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2bb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c2bb-116">-Name</span></span>
<span data-ttu-id="9c2bb-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="9c2bb-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="9c2bb-118">-RewriteRule</span></span>
<span data-ttu-id="9c2bb-119">Lista de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="9c2bb-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="9c2bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2bb-120">CommonParameters</span></span>
<span data-ttu-id="9c2bb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2bb-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2bb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2bb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c2bb-123">INPUTS</span></span>

### <span data-ttu-id="9c2bb-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c2bb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c2bb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c2bb-125">OUTPUTS</span></span>

### <span data-ttu-id="9c2bb-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c2bb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c2bb-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c2bb-127">NOTES</span></span>

## <span data-ttu-id="9c2bb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c2bb-128">RELATED LINKS</span></span>

[<span data-ttu-id="9c2bb-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9c2bb-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9c2bb-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9c2bb-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9c2bb-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9c2bb-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9c2bb-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9c2bb-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9c2bb-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c2bb-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
