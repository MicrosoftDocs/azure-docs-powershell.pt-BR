---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771911"
---
# <span data-ttu-id="2896b-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2896b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2896b-102">SYNOPSIS</span></span>
<span data-ttu-id="2896b-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2896b-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="2896b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2896b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2896b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2896b-105">DESCRIPTION</span></span>
<span data-ttu-id="2896b-106">**O cmdlet New-AzApplicationGatewayRewriteRuleSet** cria um conjunto de regras de regravação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="2896b-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="2896b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2896b-107">EXAMPLES</span></span>

### <span data-ttu-id="2896b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2896b-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="2896b-109">Esse comando cria um conjunto de regras de regravação chamado ruleset1 e armazena o resultado na variável chamada $ruleset.</span><span class="sxs-lookup"><span data-stu-id="2896b-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="2896b-110">OS</span><span class="sxs-lookup"><span data-stu-id="2896b-110">PARAMETERS</span></span>

### <span data-ttu-id="2896b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2896b-111">-DefaultProfile</span></span>
<span data-ttu-id="2896b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2896b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2896b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2896b-113">-Name</span></span>
<span data-ttu-id="2896b-114">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="2896b-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="2896b-115">-RewriteRule</span></span>
<span data-ttu-id="2896b-116">Lista de regras de regravação</span><span class="sxs-lookup"><span data-stu-id="2896b-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="2896b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2896b-117">CommonParameters</span></span>
<span data-ttu-id="2896b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2896b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2896b-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2896b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2896b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2896b-120">INPUTS</span></span>

### <span data-ttu-id="2896b-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2896b-121">None</span></span>

## <span data-ttu-id="2896b-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2896b-122">OUTPUTS</span></span>

### <span data-ttu-id="2896b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2896b-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2896b-124">NOTES</span></span>

## <span data-ttu-id="2896b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2896b-125">RELATED LINKS</span></span>

[<span data-ttu-id="2896b-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2896b-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2896b-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2896b-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2896b-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2896b-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2896b-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2896b-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2896b-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2896b-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2896b-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)