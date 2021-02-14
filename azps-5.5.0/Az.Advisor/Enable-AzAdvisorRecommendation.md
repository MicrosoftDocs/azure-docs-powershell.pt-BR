---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116696"
---
# <span data-ttu-id="108f6-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="108f6-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="108f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="108f6-102">SYNOPSIS</span></span>
<span data-ttu-id="108f6-103">Habilita as recomendações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="108f6-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="108f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="108f6-104">SYNTAX</span></span>

### <span data-ttu-id="108f6-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="108f6-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108f6-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="108f6-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108f6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="108f6-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108f6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="108f6-108">DESCRIPTION</span></span>
<span data-ttu-id="108f6-109">Esse cmdlet habilita uma recomendação suprimida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="108f6-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="108f6-110">Você também pode remover todas as suprimições associadas a uma recomendação.</span><span class="sxs-lookup"><span data-stu-id="108f6-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="108f6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="108f6-111">EXAMPLES</span></span>

### <span data-ttu-id="108f6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="108f6-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="108f6-113">Remove todas as suprimições da determinada recomendação com o nome "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="108f6-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="108f6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="108f6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="108f6-115">Remove todas as suprimições para as determinadas recomendações passadas do pipeline.</span><span class="sxs-lookup"><span data-stu-id="108f6-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="108f6-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="108f6-116">PARAMETERS</span></span>

### <span data-ttu-id="108f6-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="108f6-117">-Confirm</span></span>
<span data-ttu-id="108f6-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108f6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108f6-119">-DefaultProfile</span></span>
<span data-ttu-id="108f6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="108f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="108f6-121">-InputObject</span></span>
<span data-ttu-id="108f6-122">O tipo de objeto do PowerShell PsAzureAdvisorResourceRecommendationBase retornado por Get-AzAdvisorRecommendation chamada.</span><span class="sxs-lookup"><span data-stu-id="108f6-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-123">-Nomeda Recomendação</span><span class="sxs-lookup"><span data-stu-id="108f6-123">-RecommendationName</span></span>
<span data-ttu-id="108f6-124">Nomedo Recurso da recomendação.</span><span class="sxs-lookup"><span data-stu-id="108f6-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="108f6-125">-ResourceId</span></span>
<span data-ttu-id="108f6-126">ID da recomendação a ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="108f6-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108f6-127">-WhatIf</span></span>
<span data-ttu-id="108f6-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="108f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108f6-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="108f6-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108f6-130">CommonParameters</span></span>
<span data-ttu-id="108f6-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="108f6-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="108f6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108f6-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="108f6-133">INPUTS</span></span>

### <span data-ttu-id="108f6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="108f6-134">System.String</span></span>

### <span data-ttu-id="108f6-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="108f6-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="108f6-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="108f6-136">OUTPUTS</span></span>

### <span data-ttu-id="108f6-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="108f6-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="108f6-138">Notas</span><span class="sxs-lookup"><span data-stu-id="108f6-138">NOTES</span></span>

## <span data-ttu-id="108f6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="108f6-139">RELATED LINKS</span></span>
