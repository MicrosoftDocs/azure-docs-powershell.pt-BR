---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117406"
---
# <span data-ttu-id="c332d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c332d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="c332d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c332d-102">SYNOPSIS</span></span>
<span data-ttu-id="c332d-103">Cria uma configuração de título de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c332d-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="c332d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c332d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c332d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c332d-105">DESCRIPTION</span></span>
<span data-ttu-id="c332d-106">**O cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** cria uma ação de regra de reescrita definida para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c332d-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="c332d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c332d-107">EXAMPLES</span></span>

### <span data-ttu-id="c332d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c332d-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="c332d-109">Esse comando cria uma configuração de título de regra de reescrita e armazena o resultado na variável chamada $hc.</span><span class="sxs-lookup"><span data-stu-id="c332d-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="c332d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c332d-110">PARAMETERS</span></span>

### <span data-ttu-id="c332d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c332d-111">-DefaultProfile</span></span>
<span data-ttu-id="c332d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c332d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c332d-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c332d-113">-HeaderName</span></span>
<span data-ttu-id="c332d-114">Nome do Título para reescrever</span><span class="sxs-lookup"><span data-stu-id="c332d-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="c332d-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="c332d-115">-HeaderValue</span></span>
<span data-ttu-id="c332d-116">Valor de cabeça para o conjunto para o nome de determinado header.</span><span class="sxs-lookup"><span data-stu-id="c332d-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="c332d-117">O header será excluído se isso for omitido</span><span class="sxs-lookup"><span data-stu-id="c332d-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="c332d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c332d-118">CommonParameters</span></span>
<span data-ttu-id="c332d-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c332d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c332d-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c332d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c332d-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="c332d-121">INPUTS</span></span>

### <span data-ttu-id="c332d-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c332d-122">None</span></span>

## <span data-ttu-id="c332d-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="c332d-123">OUTPUTS</span></span>

### <span data-ttu-id="c332d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c332d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="c332d-125">Notas</span><span class="sxs-lookup"><span data-stu-id="c332d-125">NOTES</span></span>

## <span data-ttu-id="c332d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c332d-126">RELATED LINKS</span></span>

[<span data-ttu-id="c332d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c332d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c332d-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c332d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c332d-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c332d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c332d-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c332d-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c332d-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c332d-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c332d-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c332d-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c332d-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c332d-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
