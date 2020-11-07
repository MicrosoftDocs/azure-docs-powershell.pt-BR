---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771919"
---
# <span data-ttu-id="0c773-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0c773-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="0c773-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c773-102">SYNOPSIS</span></span>
<span data-ttu-id="0c773-103">Cria uma ação de regra de regravação definida para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c773-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="0c773-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c773-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c773-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c773-105">DESCRIPTION</span></span>
<span data-ttu-id="0c773-106">**O cmdlet New-AzApplicationGatewayRewriteRuleActionSet** cria uma ação de regra de regravação definida para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c773-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="0c773-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c773-107">EXAMPLES</span></span>

### <span data-ttu-id="0c773-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c773-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="0c773-109">Esse comando cria uma ação de regra de regravação definida e armazena o resultado na variável chamada $action.</span><span class="sxs-lookup"><span data-stu-id="0c773-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="0c773-110">OS</span><span class="sxs-lookup"><span data-stu-id="0c773-110">PARAMETERS</span></span>

### <span data-ttu-id="0c773-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c773-111">-DefaultProfile</span></span>
<span data-ttu-id="0c773-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c773-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c773-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c773-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="0c773-114">Lista de configurações de cabeçalho de solicitação</span><span class="sxs-lookup"><span data-stu-id="0c773-114">List of request header configurations</span></span>

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

### <span data-ttu-id="0c773-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c773-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="0c773-116">Lista de configurações de cabeçalho de resposta</span><span class="sxs-lookup"><span data-stu-id="0c773-116">List of response header configurations</span></span>

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

### <span data-ttu-id="0c773-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c773-117">CommonParameters</span></span>
<span data-ttu-id="0c773-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c773-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c773-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c773-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c773-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c773-120">INPUTS</span></span>

### <span data-ttu-id="0c773-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0c773-121">None</span></span>

## <span data-ttu-id="0c773-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c773-122">OUTPUTS</span></span>

### <span data-ttu-id="0c773-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0c773-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="0c773-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c773-124">NOTES</span></span>

## <span data-ttu-id="0c773-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c773-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c773-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c773-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0c773-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c773-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0c773-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c773-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0c773-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c773-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0c773-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c773-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0c773-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0c773-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0c773-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c773-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
