---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117407"
---
# <span data-ttu-id="0cec5-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="0cec5-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="0cec5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cec5-102">SYNOPSIS</span></span>
<span data-ttu-id="0cec5-103">Adiciona uma condição à Regra Reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0cec5-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="0cec5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cec5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cec5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cec5-105">DESCRIPTION</span></span>
<span data-ttu-id="0cec5-106">**O cmdlet AzApplicationGatewayRewriteRuleCondition** cria uma condição de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cec5-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="0cec5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0cec5-107">EXAMPLES</span></span>

### <span data-ttu-id="0cec5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0cec5-108">Example 1</span></span>
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
<span data-ttu-id="0cec5-109">Esse comando cria uma condição em uma regra de reescrita e armazena o resultado na variável chamada $condition.</span><span class="sxs-lookup"><span data-stu-id="0cec5-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="0cec5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cec5-110">PARAMETERS</span></span>

### <span data-ttu-id="0cec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cec5-111">-DefaultProfile</span></span>
<span data-ttu-id="0cec5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cec5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cec5-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="0cec5-113">-IgnoreCase</span></span>
<span data-ttu-id="0cec5-114">Definir esse sinalizador para ignorar as ocorrências no padrão</span><span class="sxs-lookup"><span data-stu-id="0cec5-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="0cec5-115">-Negar</span><span class="sxs-lookup"><span data-stu-id="0cec5-115">-Negate</span></span>
<span data-ttu-id="0cec5-116">Definir esse sinalizador para negar a validação de condição</span><span class="sxs-lookup"><span data-stu-id="0cec5-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="0cec5-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="0cec5-117">-Pattern</span></span>
<span data-ttu-id="0cec5-118">Padrão a ser buscado no Header Variável</span><span class="sxs-lookup"><span data-stu-id="0cec5-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="0cec5-119">-Variável</span><span class="sxs-lookup"><span data-stu-id="0cec5-119">-Variable</span></span>
<span data-ttu-id="0cec5-120">Nome do Header para definir uma condição</span><span class="sxs-lookup"><span data-stu-id="0cec5-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="0cec5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cec5-121">CommonParameters</span></span>
<span data-ttu-id="0cec5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cec5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0cec5-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cec5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cec5-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="0cec5-124">INPUTS</span></span>

### <span data-ttu-id="0cec5-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0cec5-125">None</span></span>

## <span data-ttu-id="0cec5-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="0cec5-126">OUTPUTS</span></span>

### <span data-ttu-id="0cec5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="0cec5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="0cec5-128">Notas</span><span class="sxs-lookup"><span data-stu-id="0cec5-128">NOTES</span></span>

## <span data-ttu-id="0cec5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cec5-129">RELATED LINKS</span></span>
[<span data-ttu-id="0cec5-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0cec5-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0cec5-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0cec5-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0cec5-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0cec5-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0cec5-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0cec5-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0cec5-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
