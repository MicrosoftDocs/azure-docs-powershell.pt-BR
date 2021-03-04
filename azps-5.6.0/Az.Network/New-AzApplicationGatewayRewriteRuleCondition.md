---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891795"
---
# <span data-ttu-id="18b50-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="18b50-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="18b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b50-102">SYNOPSIS</span></span>
<span data-ttu-id="18b50-103">Adiciona uma condição ao RewriteRule para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18b50-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="18b50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18b50-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18b50-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18b50-105">DESCRIPTION</span></span>
<span data-ttu-id="18b50-106">O cmdlet **AzApplicationGatewayRewriteRuleCondition** cria uma condição de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="18b50-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="18b50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18b50-107">EXAMPLES</span></span>

### <span data-ttu-id="18b50-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18b50-108">Example 1</span></span>
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
<span data-ttu-id="18b50-109">Este comando cria uma condição em uma regra de reescrita e armazena o resultado na variável chamada $condition.</span><span class="sxs-lookup"><span data-stu-id="18b50-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="18b50-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18b50-110">PARAMETERS</span></span>

### <span data-ttu-id="18b50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b50-111">-DefaultProfile</span></span>
<span data-ttu-id="18b50-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18b50-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b50-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="18b50-113">-IgnoreCase</span></span>
<span data-ttu-id="18b50-114">Definir esse sinalizador para ignorar o caso no padrão</span><span class="sxs-lookup"><span data-stu-id="18b50-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="18b50-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="18b50-115">-Negate</span></span>
<span data-ttu-id="18b50-116">Definir esse sinalizador para negar a validação da condição</span><span class="sxs-lookup"><span data-stu-id="18b50-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="18b50-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="18b50-117">-Pattern</span></span>
<span data-ttu-id="18b50-118">Padrão a ser buscado no Header Variável</span><span class="sxs-lookup"><span data-stu-id="18b50-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="18b50-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="18b50-119">-Variable</span></span>
<span data-ttu-id="18b50-120">Nome do Header para definir a condição nele</span><span class="sxs-lookup"><span data-stu-id="18b50-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="18b50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b50-121">CommonParameters</span></span>
<span data-ttu-id="18b50-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18b50-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b50-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b50-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18b50-124">INPUTS</span></span>

### <span data-ttu-id="18b50-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="18b50-125">None</span></span>

## <span data-ttu-id="18b50-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18b50-126">OUTPUTS</span></span>

### <span data-ttu-id="18b50-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="18b50-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="18b50-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="18b50-128">NOTES</span></span>

## <span data-ttu-id="18b50-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18b50-129">RELATED LINKS</span></span>
[<span data-ttu-id="18b50-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18b50-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18b50-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18b50-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18b50-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18b50-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18b50-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18b50-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18b50-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18b50-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18b50-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="18b50-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="18b50-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="18b50-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
