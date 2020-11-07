---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: d003bd63813fa1b3b0b7d4ffc63b591655b3ff09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771915"
---
# <span data-ttu-id="a2bd5-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2bd5-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="a2bd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bd5-103">Cria uma configuração de cabeçalho de regra de regravação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="a2bd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2bd5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2bd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="a2bd5-106">**O cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** cria uma ação de regra de regravação definida para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="a2bd5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2bd5-107">EXAMPLES</span></span>

### <span data-ttu-id="a2bd5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2bd5-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="a2bd5-109">Esse comando cria uma configuração de cabeçalho de regra de regravação e armazena o resultado na variável chamada $hc.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="a2bd5-110">OS</span><span class="sxs-lookup"><span data-stu-id="a2bd5-110">PARAMETERS</span></span>

### <span data-ttu-id="a2bd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bd5-111">-DefaultProfile</span></span>
<span data-ttu-id="a2bd5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2bd5-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="a2bd5-113">-HeaderName</span></span>
<span data-ttu-id="a2bd5-114">Nome do cabeçalho a ser regravado</span><span class="sxs-lookup"><span data-stu-id="a2bd5-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="a2bd5-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="a2bd5-115">-HeaderValue</span></span>
<span data-ttu-id="a2bd5-116">Valor do cabeçalho para o conjunto do nome do cabeçalho especificado.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="a2bd5-117">O cabeçalho será excluído se for omitido</span><span class="sxs-lookup"><span data-stu-id="a2bd5-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="a2bd5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bd5-118">CommonParameters</span></span>
<span data-ttu-id="a2bd5-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2bd5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bd5-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2bd5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bd5-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2bd5-121">INPUTS</span></span>

### <span data-ttu-id="a2bd5-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a2bd5-122">None</span></span>

## <span data-ttu-id="a2bd5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2bd5-123">OUTPUTS</span></span>

### <span data-ttu-id="a2bd5-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2bd5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="a2bd5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2bd5-125">NOTES</span></span>

## <span data-ttu-id="a2bd5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2bd5-126">RELATED LINKS</span></span>

[<span data-ttu-id="a2bd5-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a2bd5-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a2bd5-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a2bd5-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a2bd5-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a2bd5-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a2bd5-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a2bd5-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a2bd5-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
