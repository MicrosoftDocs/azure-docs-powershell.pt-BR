---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772111"
---
# <span data-ttu-id="d8a8a-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d8a8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a8a-103">Adiciona um conjunto de regras de regravação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="d8a8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8a8a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a8a-106">O cmdlet **Add-AzApplicationGatewayRewriteRuleSet** adiciona uma regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="d8a8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8a8a-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a8a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8a8a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="d8a8a-109">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d8a8a-110">O segundo comando adiciona o conjunto de regras de regravação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="d8a8a-111">OS</span><span class="sxs-lookup"><span data-stu-id="d8a8a-111">PARAMETERS</span></span>

### <span data-ttu-id="d8a8a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8a8a-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8a8a-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8a8a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d8a8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a8a-114">-DefaultProfile</span></span>
<span data-ttu-id="d8a8a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a8a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8a8a-116">-Name</span></span>
<span data-ttu-id="d8a8a-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="d8a8a-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8a8a-118">-RewriteRule</span></span>
<span data-ttu-id="d8a8a-119">Lista de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="d8a8a-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="d8a8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a8a-120">CommonParameters</span></span>
<span data-ttu-id="d8a8a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a8a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a8a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a8a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8a8a-123">INPUTS</span></span>

### <span data-ttu-id="d8a8a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8a8a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8a8a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8a8a-125">OUTPUTS</span></span>

### <span data-ttu-id="d8a8a-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8a8a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8a8a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8a8a-127">NOTES</span></span>

## <span data-ttu-id="d8a8a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8a8a-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8a8a-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8a8a-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8a8a-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8a8a-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8a8a-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8a8a-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d8a8a-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d8a8a-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d8a8a-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8a8a-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)