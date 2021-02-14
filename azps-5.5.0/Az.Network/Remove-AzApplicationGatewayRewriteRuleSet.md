---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117356"
---
# <span data-ttu-id="98b34-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="98b34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98b34-102">SYNOPSIS</span></span>
<span data-ttu-id="98b34-103">Remove um conjunto de regras de reescrita de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98b34-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="98b34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b34-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98b34-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="98b34-105">DESCRIPTION</span></span>
<span data-ttu-id="98b34-106">O cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** remove uma regra de reescrita definida de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="98b34-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="98b34-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98b34-107">EXAMPLES</span></span>

### <span data-ttu-id="98b34-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98b34-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="98b34-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98b34-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="98b34-110">O segundo comando remove o conjunto de regras de reescrita chamado RuleSet02 do gateway de aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="98b34-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="98b34-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b34-111">PARAMETERS</span></span>

### <span data-ttu-id="98b34-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98b34-112">-ApplicationGateway</span></span>
<span data-ttu-id="98b34-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="98b34-113">The applicationGateway</span></span>

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

### <span data-ttu-id="98b34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b34-114">-DefaultProfile</span></span>
<span data-ttu-id="98b34-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98b34-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98b34-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="98b34-116">-Name</span></span>
<span data-ttu-id="98b34-117">O nome do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="98b34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b34-118">CommonParameters</span></span>
<span data-ttu-id="98b34-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b34-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b34-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b34-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="98b34-121">INPUTS</span></span>

### <span data-ttu-id="98b34-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98b34-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98b34-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="98b34-123">OUTPUTS</span></span>

### <span data-ttu-id="98b34-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98b34-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98b34-125">Notas</span><span class="sxs-lookup"><span data-stu-id="98b34-125">NOTES</span></span>

## <span data-ttu-id="98b34-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98b34-126">RELATED LINKS</span></span>

[<span data-ttu-id="98b34-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98b34-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98b34-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98b34-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98b34-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98b34-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="98b34-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="98b34-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="98b34-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="98b34-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98b34-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
