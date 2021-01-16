---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271769"
---
# <span data-ttu-id="01658-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="01658-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="01658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01658-102">SYNOPSIS</span></span>
<span data-ttu-id="01658-103">Cria uma configuração de cabeçalho de regra de regravação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01658-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="01658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01658-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01658-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01658-105">DESCRIPTION</span></span>
<span data-ttu-id="01658-106">**O cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** cria uma ação de regra de regravação definida para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="01658-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="01658-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01658-107">EXAMPLES</span></span>

### <span data-ttu-id="01658-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01658-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="01658-109">Esse comando cria uma configuração de cabeçalho de regra de regravação e armazena o resultado na variável chamada $hc.</span><span class="sxs-lookup"><span data-stu-id="01658-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="01658-110">OS</span><span class="sxs-lookup"><span data-stu-id="01658-110">PARAMETERS</span></span>

### <span data-ttu-id="01658-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01658-111">-DefaultProfile</span></span>
<span data-ttu-id="01658-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01658-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01658-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="01658-113">-HeaderName</span></span>
<span data-ttu-id="01658-114">Nome do cabeçalho a ser regravado</span><span class="sxs-lookup"><span data-stu-id="01658-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="01658-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="01658-115">-HeaderValue</span></span>
<span data-ttu-id="01658-116">Valor do cabeçalho para o conjunto do nome do cabeçalho especificado.</span><span class="sxs-lookup"><span data-stu-id="01658-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="01658-117">O cabeçalho será excluído se for omitido</span><span class="sxs-lookup"><span data-stu-id="01658-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="01658-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01658-118">CommonParameters</span></span>
<span data-ttu-id="01658-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01658-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01658-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01658-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01658-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01658-121">INPUTS</span></span>

### <span data-ttu-id="01658-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="01658-122">None</span></span>

## <span data-ttu-id="01658-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01658-123">OUTPUTS</span></span>

### <span data-ttu-id="01658-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="01658-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="01658-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01658-125">NOTES</span></span>

## <span data-ttu-id="01658-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01658-126">RELATED LINKS</span></span>

[<span data-ttu-id="01658-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01658-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01658-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01658-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01658-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01658-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01658-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01658-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01658-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01658-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01658-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="01658-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="01658-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="01658-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
