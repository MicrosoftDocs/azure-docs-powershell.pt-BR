---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264362"
---
# <span data-ttu-id="a43ca-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="a43ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a43ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a43ca-103">Modifica um conjunto de regras de regravação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a43ca-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="a43ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a43ca-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a43ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a43ca-106">O cmdlet **set-AzApplicationGatewayRewriteRuleSet** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a43ca-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="a43ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a43ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a43ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a43ca-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="a43ca-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a43ca-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a43ca-110">O segundo comando modifica o conjunto de regras de regravação do aplicativo gateway para usar as regras de regravação especificadas na variável $rule.</span><span class="sxs-lookup"><span data-stu-id="a43ca-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="a43ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="a43ca-111">PARAMETERS</span></span>

### <span data-ttu-id="a43ca-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a43ca-112">-ApplicationGateway</span></span>
<span data-ttu-id="a43ca-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a43ca-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a43ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43ca-114">-DefaultProfile</span></span>
<span data-ttu-id="a43ca-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a43ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a43ca-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a43ca-116">-Name</span></span>
<span data-ttu-id="a43ca-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="a43ca-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="a43ca-118">-RewriteRule</span></span>
<span data-ttu-id="a43ca-119">Lista de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="a43ca-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="a43ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43ca-120">CommonParameters</span></span>
<span data-ttu-id="a43ca-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43ca-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43ca-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43ca-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a43ca-123">INPUTS</span></span>

### <span data-ttu-id="a43ca-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a43ca-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a43ca-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a43ca-125">OUTPUTS</span></span>

### <span data-ttu-id="a43ca-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a43ca-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a43ca-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a43ca-127">NOTES</span></span>

## <span data-ttu-id="a43ca-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a43ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="a43ca-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a43ca-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a43ca-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a43ca-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a43ca-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a43ca-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a43ca-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a43ca-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="a43ca-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a43ca-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
