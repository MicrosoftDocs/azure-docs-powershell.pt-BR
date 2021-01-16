---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262371"
---
# <span data-ttu-id="d2660-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d2660-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d2660-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2660-102">SYNOPSIS</span></span>
<span data-ttu-id="d2660-103">Cria uma ação de regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2660-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="d2660-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2660-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2660-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2660-105">DESCRIPTION</span></span>
<span data-ttu-id="d2660-106">**O cmdlet New-AzApplicationGatewayRewriteRuleActionSet** cria uma ação de regra de regravação definida para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2660-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="d2660-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2660-107">EXAMPLES</span></span>

### <span data-ttu-id="d2660-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2660-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="d2660-109">Esse comando cria uma ação de regra de regravação definida e armazena o resultado na variável chamada $action.</span><span class="sxs-lookup"><span data-stu-id="d2660-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="d2660-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2660-110">PARAMETERS</span></span>

### <span data-ttu-id="d2660-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2660-111">-DefaultProfile</span></span>
<span data-ttu-id="d2660-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2660-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2660-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2660-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="d2660-114">Lista de configurações de cabeçalho de solicitação</span><span class="sxs-lookup"><span data-stu-id="d2660-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2660-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2660-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="d2660-116">Lista de configurações de cabeçalho de resposta</span><span class="sxs-lookup"><span data-stu-id="d2660-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2660-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2660-117">-UrlConfiguration</span></span>
<span data-ttu-id="d2660-118">Configuração de URL para conjunto de ações</span><span class="sxs-lookup"><span data-stu-id="d2660-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2660-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2660-119">CommonParameters</span></span>
<span data-ttu-id="d2660-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2660-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2660-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2660-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2660-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2660-122">INPUTS</span></span>

### <span data-ttu-id="d2660-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2660-123">None</span></span>

## <span data-ttu-id="d2660-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2660-124">OUTPUTS</span></span>

### <span data-ttu-id="d2660-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d2660-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d2660-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2660-126">NOTES</span></span>

## <span data-ttu-id="d2660-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2660-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2660-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2660-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2660-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2660-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2660-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2660-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2660-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2660-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2660-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2660-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2660-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d2660-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d2660-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2660-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="d2660-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2660-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)