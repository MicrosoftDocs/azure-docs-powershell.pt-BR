---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118397"
---
# <span data-ttu-id="5e41f-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="5e41f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e41f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e41f-103">Adiciona uma regra de reescrita definida a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e41f-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="5e41f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e41f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e41f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e41f-105">DESCRIPTION</span></span>
<span data-ttu-id="5e41f-106">O **cmdlet Add-AzApplicationGatewayRewriteRuleSet** adiciona uma regra de reescrita definida a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e41f-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="5e41f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e41f-107">EXAMPLES</span></span>

### <span data-ttu-id="5e41f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e41f-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="5e41f-109">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e41f-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5e41f-110">O segundo comando adiciona a regra de reescrita definida ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e41f-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="5e41f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e41f-111">PARAMETERS</span></span>

### <span data-ttu-id="5e41f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e41f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5e41f-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e41f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5e41f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e41f-114">-DefaultProfile</span></span>
<span data-ttu-id="5e41f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e41f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e41f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e41f-116">-Name</span></span>
<span data-ttu-id="5e41f-117">O nome do RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="5e41f-118">-ReescritaRule</span><span class="sxs-lookup"><span data-stu-id="5e41f-118">-RewriteRule</span></span>
<span data-ttu-id="5e41f-119">Lista de regras de reescrita</span><span class="sxs-lookup"><span data-stu-id="5e41f-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="5e41f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e41f-120">CommonParameters</span></span>
<span data-ttu-id="5e41f-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e41f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e41f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e41f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e41f-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="5e41f-123">INPUTS</span></span>

### <span data-ttu-id="5e41f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e41f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e41f-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="5e41f-125">OUTPUTS</span></span>

### <span data-ttu-id="5e41f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e41f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e41f-127">Notas</span><span class="sxs-lookup"><span data-stu-id="5e41f-127">NOTES</span></span>

## <span data-ttu-id="5e41f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e41f-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e41f-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5e41f-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5e41f-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5e41f-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5e41f-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5e41f-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="5e41f-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5e41f-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="5e41f-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e41f-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
