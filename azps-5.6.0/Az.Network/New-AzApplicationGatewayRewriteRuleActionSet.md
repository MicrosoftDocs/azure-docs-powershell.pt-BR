---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 2c5fa5f4c12a44d1efc12e75dfa3901dce061f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892748"
---
# <span data-ttu-id="d143b-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d143b-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d143b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d143b-102">SYNOPSIS</span></span>
<span data-ttu-id="d143b-103">Cria um conjunto de ações de regra de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d143b-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="d143b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d143b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d143b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d143b-105">DESCRIPTION</span></span>
<span data-ttu-id="d143b-106">O cmdlet **New-AzApplicationGatewayRewriteRuleActionSet** cria um conjunto de ações de regra de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d143b-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="d143b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d143b-107">EXAMPLES</span></span>

### <span data-ttu-id="d143b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d143b-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="d143b-109">Este comando cria um conjunto de ações de regra de regra de reescrita e armazena o resultado na variável chamada $action.</span><span class="sxs-lookup"><span data-stu-id="d143b-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="d143b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d143b-110">PARAMETERS</span></span>

### <span data-ttu-id="d143b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d143b-111">-DefaultProfile</span></span>
<span data-ttu-id="d143b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d143b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d143b-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d143b-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="d143b-114">Lista de configurações de header de solicitação</span><span class="sxs-lookup"><span data-stu-id="d143b-114">List of request header configurations</span></span>

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

### <span data-ttu-id="d143b-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d143b-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="d143b-116">Lista de configurações de header de resposta</span><span class="sxs-lookup"><span data-stu-id="d143b-116">List of response header configurations</span></span>

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

### <span data-ttu-id="d143b-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d143b-117">-UrlConfiguration</span></span>
<span data-ttu-id="d143b-118">Configuração de URL para conjunto de ações</span><span class="sxs-lookup"><span data-stu-id="d143b-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="d143b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d143b-119">CommonParameters</span></span>
<span data-ttu-id="d143b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d143b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d143b-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d143b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d143b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d143b-122">INPUTS</span></span>

### <span data-ttu-id="d143b-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d143b-123">None</span></span>

## <span data-ttu-id="d143b-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d143b-124">OUTPUTS</span></span>

### <span data-ttu-id="d143b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d143b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d143b-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="d143b-126">NOTES</span></span>

## <span data-ttu-id="d143b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d143b-127">RELATED LINKS</span></span>

[<span data-ttu-id="d143b-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d143b-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d143b-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d143b-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d143b-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d143b-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d143b-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d143b-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d143b-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d143b-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d143b-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d143b-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d143b-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d143b-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="d143b-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d143b-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)