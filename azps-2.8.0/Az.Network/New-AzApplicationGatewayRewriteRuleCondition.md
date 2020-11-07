---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771916"
---
# <span data-ttu-id="24b96-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="24b96-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="24b96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24b96-102">SYNOPSIS</span></span>
<span data-ttu-id="24b96-103">Adiciona uma condição ao RewriteRule para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24b96-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="24b96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24b96-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24b96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24b96-105">DESCRIPTION</span></span>
<span data-ttu-id="24b96-106">**O cmdlet AzApplicationGatewayRewriteRuleCondition** cria uma condição de regra de regravação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="24b96-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="24b96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24b96-107">EXAMPLES</span></span>

### <span data-ttu-id="24b96-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24b96-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="24b96-109">Esse comando cria uma condição em uma regra de regravação e armazena o resultado na variável chamada $condition.</span><span class="sxs-lookup"><span data-stu-id="24b96-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="24b96-110">OS</span><span class="sxs-lookup"><span data-stu-id="24b96-110">PARAMETERS</span></span>

### <span data-ttu-id="24b96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b96-111">-DefaultProfile</span></span>
<span data-ttu-id="24b96-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24b96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="24b96-113">-IgnoreCase</span></span>
<span data-ttu-id="24b96-114">Definir este sinalizador para ignorar maiúsculas e minúsculas no padrão</span><span class="sxs-lookup"><span data-stu-id="24b96-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-115">-Negar</span><span class="sxs-lookup"><span data-stu-id="24b96-115">-Negate</span></span>
<span data-ttu-id="24b96-116">Defina esse sinalizador para negar a validação da condição</span><span class="sxs-lookup"><span data-stu-id="24b96-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-117">-Padrão</span><span class="sxs-lookup"><span data-stu-id="24b96-117">-Pattern</span></span>
<span data-ttu-id="24b96-118">Padrão para procurar no cabeçalho da variável</span><span class="sxs-lookup"><span data-stu-id="24b96-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-119">-Variável</span><span class="sxs-lookup"><span data-stu-id="24b96-119">-Variable</span></span>
<span data-ttu-id="24b96-120">Nome do cabeçalho para definir a condição nele</span><span class="sxs-lookup"><span data-stu-id="24b96-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b96-121">CommonParameters</span></span>
<span data-ttu-id="24b96-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24b96-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b96-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b96-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24b96-124">INPUTS</span></span>

### <span data-ttu-id="24b96-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="24b96-125">None</span></span>

## <span data-ttu-id="24b96-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24b96-126">OUTPUTS</span></span>

### <span data-ttu-id="24b96-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="24b96-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="24b96-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24b96-128">NOTES</span></span>

## <span data-ttu-id="24b96-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24b96-129">RELATED LINKS</span></span>
[<span data-ttu-id="24b96-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b96-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24b96-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b96-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24b96-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b96-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24b96-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b96-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24b96-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b96-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="24b96-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="24b96-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="24b96-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="24b96-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)