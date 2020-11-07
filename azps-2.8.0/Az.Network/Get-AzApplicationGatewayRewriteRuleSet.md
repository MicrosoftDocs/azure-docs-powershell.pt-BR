---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 35338b5fa179e916bfb52f2529a12d5be1665e89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771797"
---
# <span data-ttu-id="57658-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="57658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57658-102">SYNOPSIS</span></span>
<span data-ttu-id="57658-103">Obtém o conjunto de regras de regravação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57658-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="57658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57658-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57658-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57658-105">DESCRIPTION</span></span>
<span data-ttu-id="57658-106">Obtém o conjunto de regras de regravação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57658-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="57658-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57658-107">EXAMPLES</span></span>

### <span data-ttu-id="57658-108">Exemplo 1: obter um conjunto de regras de regravação específico</span><span class="sxs-lookup"><span data-stu-id="57658-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="57658-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="57658-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="57658-110">O segundo comando obtém o conjunto de regras Rewrite chamado RuleSet01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="57658-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="57658-111">OS</span><span class="sxs-lookup"><span data-stu-id="57658-111">PARAMETERS</span></span>

### <span data-ttu-id="57658-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57658-112">-ApplicationGateway</span></span>
<span data-ttu-id="57658-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="57658-113">The applicationGateway</span></span>

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

### <span data-ttu-id="57658-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57658-114">-DefaultProfile</span></span>
<span data-ttu-id="57658-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57658-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57658-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="57658-116">-Name</span></span>
<span data-ttu-id="57658-117">O nome do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="57658-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57658-118">CommonParameters</span></span>
<span data-ttu-id="57658-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57658-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57658-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57658-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57658-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57658-121">INPUTS</span></span>

### <span data-ttu-id="57658-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57658-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57658-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57658-123">OUTPUTS</span></span>

### <span data-ttu-id="57658-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="57658-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57658-125">NOTES</span></span>

## <span data-ttu-id="57658-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57658-126">RELATED LINKS</span></span>

[<span data-ttu-id="57658-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57658-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57658-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57658-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57658-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57658-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="57658-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="57658-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="57658-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="57658-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="57658-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
