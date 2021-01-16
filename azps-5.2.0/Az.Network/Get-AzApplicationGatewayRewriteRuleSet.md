---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256672"
---
# <span data-ttu-id="546d2-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="546d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="546d2-102">SYNOPSIS</span></span>
<span data-ttu-id="546d2-103">Obtém o conjunto de regras de regravação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="546d2-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="546d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="546d2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="546d2-105">DESCRIPTION</span></span>
<span data-ttu-id="546d2-106">Obtém o conjunto de regras de regravação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="546d2-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="546d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="546d2-107">EXAMPLES</span></span>

### <span data-ttu-id="546d2-108">Exemplo 1: obter um conjunto de regras de regravação específico</span><span class="sxs-lookup"><span data-stu-id="546d2-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="546d2-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="546d2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="546d2-110">O segundo comando obtém o conjunto de regras Rewrite chamado RuleSet01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="546d2-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="546d2-111">OS</span><span class="sxs-lookup"><span data-stu-id="546d2-111">PARAMETERS</span></span>

### <span data-ttu-id="546d2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="546d2-112">-ApplicationGateway</span></span>
<span data-ttu-id="546d2-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="546d2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="546d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546d2-114">-DefaultProfile</span></span>
<span data-ttu-id="546d2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="546d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546d2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="546d2-116">-Name</span></span>
<span data-ttu-id="546d2-117">O nome do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="546d2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546d2-118">CommonParameters</span></span>
<span data-ttu-id="546d2-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546d2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546d2-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="546d2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546d2-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="546d2-121">INPUTS</span></span>

### <span data-ttu-id="546d2-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="546d2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="546d2-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="546d2-123">OUTPUTS</span></span>

### <span data-ttu-id="546d2-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="546d2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="546d2-125">NOTES</span></span>

## <span data-ttu-id="546d2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="546d2-126">RELATED LINKS</span></span>

[<span data-ttu-id="546d2-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="546d2-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="546d2-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="546d2-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="546d2-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="546d2-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="546d2-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="546d2-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="546d2-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="546d2-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="546d2-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
