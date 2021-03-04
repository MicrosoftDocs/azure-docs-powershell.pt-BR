---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890818"
---
# <span data-ttu-id="9586d-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9586d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9586d-102">SYNOPSIS</span></span>
<span data-ttu-id="9586d-103">Obtém o conjunto de regras de regra de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9586d-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="9586d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9586d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9586d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9586d-105">DESCRIPTION</span></span>
<span data-ttu-id="9586d-106">Obtém o conjunto de regras de regra de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9586d-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="9586d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9586d-107">EXAMPLES</span></span>

### <span data-ttu-id="9586d-108">Exemplo 1 : Obter um conjunto de regras de regra de regra de reescrita específico</span><span class="sxs-lookup"><span data-stu-id="9586d-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="9586d-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9586d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="9586d-110">O segundo comando obtém o conjunto de regras de regra de reescrita denominado RuleSet01 do Gateway de Aplicativo armazenado na variável denominada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="9586d-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="9586d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9586d-111">PARAMETERS</span></span>

### <span data-ttu-id="9586d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9586d-112">-ApplicationGateway</span></span>
<span data-ttu-id="9586d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9586d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9586d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9586d-114">-DefaultProfile</span></span>
<span data-ttu-id="9586d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9586d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9586d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9586d-116">-Name</span></span>
<span data-ttu-id="9586d-117">O nome do gateway de aplicativos RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-117">The name of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9586d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9586d-118">CommonParameters</span></span>
<span data-ttu-id="9586d-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9586d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9586d-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9586d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9586d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9586d-121">INPUTS</span></span>

### <span data-ttu-id="9586d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9586d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9586d-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9586d-123">OUTPUTS</span></span>

### <span data-ttu-id="9586d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9586d-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="9586d-125">NOTES</span></span>

## <span data-ttu-id="9586d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9586d-126">RELATED LINKS</span></span>

[<span data-ttu-id="9586d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9586d-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9586d-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9586d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9586d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9586d-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9586d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9586d-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9586d-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9586d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9586d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
