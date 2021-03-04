---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: 6d5bbd0cd0b5581e129e63e7559c09751d8f91cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885985"
---
# <span data-ttu-id="059f0-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="059f0-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="059f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059f0-102">SYNOPSIS</span></span>
<span data-ttu-id="059f0-103">Cria uma configuração de header de regra de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="059f0-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="059f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="059f0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="059f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="059f0-105">DESCRIPTION</span></span>
<span data-ttu-id="059f0-106">O cmdlet **AzApplicationGatewayRewriteRuleHeaderConfiguration** cria um conjunto de ações de regra de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="059f0-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="059f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="059f0-107">EXAMPLES</span></span>

### <span data-ttu-id="059f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="059f0-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="059f0-109">Este comando cria uma configuração de header de regra de regra de reescrita e armazena o resultado na variável chamada $hc.</span><span class="sxs-lookup"><span data-stu-id="059f0-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="059f0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="059f0-110">PARAMETERS</span></span>

### <span data-ttu-id="059f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059f0-111">-DefaultProfile</span></span>
<span data-ttu-id="059f0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="059f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059f0-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="059f0-113">-HeaderName</span></span>
<span data-ttu-id="059f0-114">Nome do Header a ser regravado</span><span class="sxs-lookup"><span data-stu-id="059f0-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="059f0-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="059f0-115">-HeaderValue</span></span>
<span data-ttu-id="059f0-116">Valor de header para o conjunto para o nome do header determinado.</span><span class="sxs-lookup"><span data-stu-id="059f0-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="059f0-117">O header será excluído se isso for omitido</span><span class="sxs-lookup"><span data-stu-id="059f0-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="059f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059f0-118">CommonParameters</span></span>
<span data-ttu-id="059f0-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059f0-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059f0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059f0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="059f0-121">INPUTS</span></span>

### <span data-ttu-id="059f0-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="059f0-122">None</span></span>

## <span data-ttu-id="059f0-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="059f0-123">OUTPUTS</span></span>

### <span data-ttu-id="059f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="059f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="059f0-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="059f0-125">NOTES</span></span>

## <span data-ttu-id="059f0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="059f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="059f0-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="059f0-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="059f0-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="059f0-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="059f0-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="059f0-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="059f0-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="059f0-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="059f0-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="059f0-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="059f0-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="059f0-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="059f0-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="059f0-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
