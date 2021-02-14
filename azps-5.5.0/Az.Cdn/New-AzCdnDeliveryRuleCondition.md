---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111184"
---
# <span data-ttu-id="2bcf2-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="2bcf2-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="2bcf2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcf2-103">Cria uma condição de regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="2bcf2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bcf2-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bcf2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bcf2-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcf2-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para a criação do ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="2bcf2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2bcf2-107">EXAMPLES</span></span>

### <span data-ttu-id="2bcf2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bcf2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="2bcf2-109">Crie uma condição simples.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-109">Create a simple condition.</span></span>

## <span data-ttu-id="2bcf2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bcf2-110">PARAMETERS</span></span>

### <span data-ttu-id="2bcf2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcf2-111">-DefaultProfile</span></span>
<span data-ttu-id="2bcf2-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bcf2-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="2bcf2-113">-MatchValue</span></span>
<span data-ttu-id="2bcf2-114">Lista de possíveis valores de combinação.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcf2-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="2bcf2-115">-MatchVariable</span></span>
<span data-ttu-id="2bcf2-116">Corresponder variável da condição.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="2bcf2-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="2bcf2-117">-NegateCondition</span></span>
<span data-ttu-id="2bcf2-118">Descreve se o resultado dessa condição deve ser negativo.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcf2-119">-Operador</span><span class="sxs-lookup"><span data-stu-id="2bcf2-119">-Operator</span></span>
<span data-ttu-id="2bcf2-120">Descreve o operador a ser corresponder</span><span class="sxs-lookup"><span data-stu-id="2bcf2-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="2bcf2-121">-Seletor</span><span class="sxs-lookup"><span data-stu-id="2bcf2-121">-Selector</span></span>
<span data-ttu-id="2bcf2-122">Nome do Seletor a ser corresponder</span><span class="sxs-lookup"><span data-stu-id="2bcf2-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="2bcf2-123">-Transformar</span><span class="sxs-lookup"><span data-stu-id="2bcf2-123">-Transform</span></span>
<span data-ttu-id="2bcf2-124">Transforme para aplicar antes da correspondência.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-124">Transform to apply before matching.</span></span>
<span data-ttu-id="2bcf2-125">Os valores possíveis são Minúsculas e Maiúsculas</span><span class="sxs-lookup"><span data-stu-id="2bcf2-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="2bcf2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcf2-126">CommonParameters</span></span>
<span data-ttu-id="2bcf2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bcf2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcf2-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bcf2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcf2-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="2bcf2-129">INPUTS</span></span>

### <span data-ttu-id="2bcf2-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2bcf2-130">None</span></span>

## <span data-ttu-id="2bcf2-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="2bcf2-131">OUTPUTS</span></span>

### <span data-ttu-id="2bcf2-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="2bcf2-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="2bcf2-133">Notas</span><span class="sxs-lookup"><span data-stu-id="2bcf2-133">NOTES</span></span>

## <span data-ttu-id="2bcf2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bcf2-134">RELATED LINKS</span></span>
