---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597582"
---
# <span data-ttu-id="0beb9-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="0beb9-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="0beb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0beb9-102">SYNOPSIS</span></span>
<span data-ttu-id="0beb9-103">Cria uma condição de regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="0beb9-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="0beb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0beb9-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0beb9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0beb9-105">DESCRIPTION</span></span>
<span data-ttu-id="0beb9-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="0beb9-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="0beb9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0beb9-107">EXAMPLES</span></span>

### <span data-ttu-id="0beb9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0beb9-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="0beb9-109">Criar uma condição simples.</span><span class="sxs-lookup"><span data-stu-id="0beb9-109">Create a simple condition.</span></span>

## <span data-ttu-id="0beb9-110">OS</span><span class="sxs-lookup"><span data-stu-id="0beb9-110">PARAMETERS</span></span>

### <span data-ttu-id="0beb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0beb9-111">-DefaultProfile</span></span>
<span data-ttu-id="0beb9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0beb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0beb9-113">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="0beb9-113">-MatchValue</span></span>
<span data-ttu-id="0beb9-114">Lista de possíveis valores de correspondência.</span><span class="sxs-lookup"><span data-stu-id="0beb9-114">List of possible match values.</span></span>

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

### <span data-ttu-id="0beb9-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="0beb9-115">-MatchVariable</span></span>
<span data-ttu-id="0beb9-116">Corresponde à variável da condição.</span><span class="sxs-lookup"><span data-stu-id="0beb9-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="0beb9-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="0beb9-117">-NegateCondition</span></span>
<span data-ttu-id="0beb9-118">Descreve se o resultado dessa condição deve ser negado.</span><span class="sxs-lookup"><span data-stu-id="0beb9-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="0beb9-119">-Operador</span><span class="sxs-lookup"><span data-stu-id="0beb9-119">-Operator</span></span>
<span data-ttu-id="0beb9-120">Descreve o operador a ser correspondido</span><span class="sxs-lookup"><span data-stu-id="0beb9-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="0beb9-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="0beb9-121">-Transform</span></span>
<span data-ttu-id="0beb9-122">Transformação a ser aplicada antes da correspondência.</span><span class="sxs-lookup"><span data-stu-id="0beb9-122">Transform to apply before matching.</span></span>
<span data-ttu-id="0beb9-123">Os valores possíveis são minúsculas e maiúsculas</span><span class="sxs-lookup"><span data-stu-id="0beb9-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="0beb9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0beb9-124">CommonParameters</span></span>
<span data-ttu-id="0beb9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0beb9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0beb9-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0beb9-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0beb9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0beb9-127">INPUTS</span></span>

### <span data-ttu-id="0beb9-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0beb9-128">None</span></span>

## <span data-ttu-id="0beb9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0beb9-129">OUTPUTS</span></span>

### <span data-ttu-id="0beb9-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="0beb9-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="0beb9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0beb9-131">NOTES</span></span>

## <span data-ttu-id="0beb9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0beb9-132">RELATED LINKS</span></span>
