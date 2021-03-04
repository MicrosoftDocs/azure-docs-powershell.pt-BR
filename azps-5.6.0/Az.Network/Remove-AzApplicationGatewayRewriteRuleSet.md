---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 099abbe1f8c2a536cebff59f1c21b664bb284e8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890239"
---
# <span data-ttu-id="37040-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="37040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37040-102">SYNOPSIS</span></span>
<span data-ttu-id="37040-103">Remove um conjunto de regras de regra de regra de regra de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="37040-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="37040-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37040-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37040-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37040-105">DESCRIPTION</span></span>
<span data-ttu-id="37040-106">O cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** remove um conjunto de regras de reescrita de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="37040-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="37040-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37040-107">EXAMPLES</span></span>

### <span data-ttu-id="37040-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37040-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="37040-109">O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="37040-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="37040-110">O segundo comando remove o conjunto de regras de regra de reescrita denominado RuleSet02 do gateway de aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="37040-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="37040-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37040-111">PARAMETERS</span></span>

### <span data-ttu-id="37040-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37040-112">-ApplicationGateway</span></span>
<span data-ttu-id="37040-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37040-113">The applicationGateway</span></span>

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

### <span data-ttu-id="37040-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37040-114">-DefaultProfile</span></span>
<span data-ttu-id="37040-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37040-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37040-116">-Name</span><span class="sxs-lookup"><span data-stu-id="37040-116">-Name</span></span>
<span data-ttu-id="37040-117">O nome do gateway de aplicativos RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="37040-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37040-118">CommonParameters</span></span>
<span data-ttu-id="37040-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37040-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37040-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37040-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37040-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37040-121">INPUTS</span></span>

### <span data-ttu-id="37040-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37040-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37040-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37040-123">OUTPUTS</span></span>

### <span data-ttu-id="37040-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37040-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37040-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="37040-125">NOTES</span></span>

## <span data-ttu-id="37040-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37040-126">RELATED LINKS</span></span>

[<span data-ttu-id="37040-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37040-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37040-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37040-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37040-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37040-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="37040-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="37040-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37040-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="37040-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="37040-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
