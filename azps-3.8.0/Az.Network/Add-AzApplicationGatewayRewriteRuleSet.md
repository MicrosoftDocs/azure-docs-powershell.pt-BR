---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943786"
---
# <span data-ttu-id="c3d41-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="c3d41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3d41-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d41-103">Adiciona um conjunto de regras de regravação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3d41-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="c3d41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3d41-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3d41-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d41-106">O cmdlet **Add-AzApplicationGatewayRewriteRuleSet** adiciona uma regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3d41-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="c3d41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3d41-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d41-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d41-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="c3d41-109">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c3d41-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c3d41-110">O segundo comando adiciona o conjunto de regras de regravação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3d41-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="c3d41-111">OS</span><span class="sxs-lookup"><span data-stu-id="c3d41-111">PARAMETERS</span></span>

### <span data-ttu-id="c3d41-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d41-112">-ApplicationGateway</span></span>
<span data-ttu-id="c3d41-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d41-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c3d41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d41-114">-DefaultProfile</span></span>
<span data-ttu-id="c3d41-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d41-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3d41-116">-Name</span></span>
<span data-ttu-id="c3d41-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="c3d41-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="c3d41-118">-RewriteRule</span></span>
<span data-ttu-id="c3d41-119">Lista de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="c3d41-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="c3d41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d41-120">CommonParameters</span></span>
<span data-ttu-id="c3d41-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d41-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d41-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d41-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3d41-123">INPUTS</span></span>

### <span data-ttu-id="c3d41-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d41-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3d41-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3d41-125">OUTPUTS</span></span>

### <span data-ttu-id="c3d41-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3d41-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3d41-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3d41-127">NOTES</span></span>

## <span data-ttu-id="c3d41-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d41-128">RELATED LINKS</span></span>

[<span data-ttu-id="c3d41-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c3d41-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c3d41-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c3d41-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c3d41-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c3d41-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c3d41-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c3d41-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="c3d41-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3d41-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
