---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114382"
---
# <span data-ttu-id="d83df-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d83df-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d83df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d83df-102">SYNOPSIS</span></span>
<span data-ttu-id="d83df-103">Cria uma ação de regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d83df-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="d83df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d83df-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d83df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d83df-105">DESCRIPTION</span></span>
<span data-ttu-id="d83df-106">**O cmdlet New-AzApplicationGatewayRewriteRuleActionSet** cria uma ação de regra de regravação definida para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d83df-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="d83df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d83df-107">EXAMPLES</span></span>

### <span data-ttu-id="d83df-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d83df-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="d83df-109">Esse comando cria uma ação de regra de regravação definida e armazena o resultado na variável chamada $action.</span><span class="sxs-lookup"><span data-stu-id="d83df-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="d83df-110">OS</span><span class="sxs-lookup"><span data-stu-id="d83df-110">PARAMETERS</span></span>

### <span data-ttu-id="d83df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83df-111">-DefaultProfile</span></span>
<span data-ttu-id="d83df-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d83df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d83df-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83df-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="d83df-114">Lista de configurações de cabeçalho de solicitação</span><span class="sxs-lookup"><span data-stu-id="d83df-114">List of request header configurations</span></span>

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

### <span data-ttu-id="d83df-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83df-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="d83df-116">Lista de configurações de cabeçalho de resposta</span><span class="sxs-lookup"><span data-stu-id="d83df-116">List of response header configurations</span></span>

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

### <span data-ttu-id="d83df-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83df-117">-UrlConfiguration</span></span>
<span data-ttu-id="d83df-118">Configuração de URL para conjunto de ações</span><span class="sxs-lookup"><span data-stu-id="d83df-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="d83df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83df-119">CommonParameters</span></span>
<span data-ttu-id="d83df-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83df-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83df-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83df-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d83df-122">INPUTS</span></span>

### <span data-ttu-id="d83df-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d83df-123">None</span></span>

## <span data-ttu-id="d83df-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d83df-124">OUTPUTS</span></span>

### <span data-ttu-id="d83df-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d83df-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d83df-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d83df-126">NOTES</span></span>

## <span data-ttu-id="d83df-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d83df-127">RELATED LINKS</span></span>

[<span data-ttu-id="d83df-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d83df-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d83df-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d83df-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d83df-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d83df-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d83df-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d83df-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d83df-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d83df-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d83df-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d83df-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d83df-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83df-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="d83df-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83df-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)