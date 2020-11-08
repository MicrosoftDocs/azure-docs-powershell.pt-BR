---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111773"
---
# <span data-ttu-id="ef345-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ef345-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="ef345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef345-102">SYNOPSIS</span></span>
<span data-ttu-id="ef345-103">Cria uma condição de regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="ef345-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="ef345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef345-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef345-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef345-105">DESCRIPTION</span></span>
<span data-ttu-id="ef345-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ef345-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="ef345-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef345-107">EXAMPLES</span></span>

### <span data-ttu-id="ef345-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef345-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="ef345-109">Criar uma condição simples.</span><span class="sxs-lookup"><span data-stu-id="ef345-109">Create a simple condition.</span></span>

## <span data-ttu-id="ef345-110">OS</span><span class="sxs-lookup"><span data-stu-id="ef345-110">PARAMETERS</span></span>

### <span data-ttu-id="ef345-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef345-111">-DefaultProfile</span></span>
<span data-ttu-id="ef345-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef345-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef345-113">-Matchvalue</span><span class="sxs-lookup"><span data-stu-id="ef345-113">-MatchValue</span></span>
<span data-ttu-id="ef345-114">Lista de possíveis valores de correspondência.</span><span class="sxs-lookup"><span data-stu-id="ef345-114">List of possible match values.</span></span>

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

### <span data-ttu-id="ef345-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ef345-115">-MatchVariable</span></span>
<span data-ttu-id="ef345-116">Corresponde à variável da condição.</span><span class="sxs-lookup"><span data-stu-id="ef345-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="ef345-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="ef345-117">-NegateCondition</span></span>
<span data-ttu-id="ef345-118">Descreve se o resultado dessa condição deve ser negado.</span><span class="sxs-lookup"><span data-stu-id="ef345-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="ef345-119">-Operador</span><span class="sxs-lookup"><span data-stu-id="ef345-119">-Operator</span></span>
<span data-ttu-id="ef345-120">Descreve o operador a ser correspondido</span><span class="sxs-lookup"><span data-stu-id="ef345-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="ef345-121">-Seletor</span><span class="sxs-lookup"><span data-stu-id="ef345-121">-Selector</span></span>
<span data-ttu-id="ef345-122">Nome do seletor a ser correspondido</span><span class="sxs-lookup"><span data-stu-id="ef345-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="ef345-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="ef345-123">-Transform</span></span>
<span data-ttu-id="ef345-124">Transformação a ser aplicada antes da correspondência.</span><span class="sxs-lookup"><span data-stu-id="ef345-124">Transform to apply before matching.</span></span>
<span data-ttu-id="ef345-125">Os valores possíveis são minúsculas e maiúsculas</span><span class="sxs-lookup"><span data-stu-id="ef345-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="ef345-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef345-126">CommonParameters</span></span>
<span data-ttu-id="ef345-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef345-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef345-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef345-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef345-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef345-129">INPUTS</span></span>

### <span data-ttu-id="ef345-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ef345-130">None</span></span>

## <span data-ttu-id="ef345-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef345-131">OUTPUTS</span></span>

### <span data-ttu-id="ef345-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ef345-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="ef345-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef345-133">NOTES</span></span>

## <span data-ttu-id="ef345-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef345-134">RELATED LINKS</span></span>
