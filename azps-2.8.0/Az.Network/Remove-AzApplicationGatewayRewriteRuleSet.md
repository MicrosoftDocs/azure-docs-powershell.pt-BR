---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 7d7403fff78d04153f1c088cbdf41f61677e2e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772297"
---
# <span data-ttu-id="a49fe-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="a49fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a49fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a49fe-103">Remove um conjunto de regras de regravação de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a49fe-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="a49fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a49fe-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a49fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a49fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a49fe-106">O cmdlet **Remove-AzApplicationGatewayRewriteRuleSet** remove um conjunto de regras de regravação de um aplicativo de gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="a49fe-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="a49fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a49fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a49fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a49fe-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="a49fe-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a49fe-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a49fe-110">O segundo comando Remove o conjunto de regras Rewrite chamado RuleSet02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a49fe-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a49fe-111">OS</span><span class="sxs-lookup"><span data-stu-id="a49fe-111">PARAMETERS</span></span>

### <span data-ttu-id="a49fe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a49fe-112">-ApplicationGateway</span></span>
<span data-ttu-id="a49fe-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a49fe-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a49fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49fe-114">-DefaultProfile</span></span>
<span data-ttu-id="a49fe-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a49fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a49fe-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a49fe-116">-Name</span></span>
<span data-ttu-id="a49fe-117">O nome do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="a49fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49fe-118">CommonParameters</span></span>
<span data-ttu-id="a49fe-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49fe-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a49fe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49fe-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a49fe-121">INPUTS</span></span>

### <span data-ttu-id="a49fe-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a49fe-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a49fe-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a49fe-123">OUTPUTS</span></span>

### <span data-ttu-id="a49fe-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a49fe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a49fe-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a49fe-125">NOTES</span></span>

## <span data-ttu-id="a49fe-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a49fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="a49fe-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a49fe-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a49fe-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a49fe-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a49fe-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a49fe-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a49fe-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a49fe-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="a49fe-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a49fe-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)