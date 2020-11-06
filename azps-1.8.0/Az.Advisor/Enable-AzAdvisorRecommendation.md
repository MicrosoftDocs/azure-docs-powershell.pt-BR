---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 05d74b254645a970389aae859d60583c53c07670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595762"
---
# <span data-ttu-id="47721-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="47721-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="47721-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47721-102">SYNOPSIS</span></span>
<span data-ttu-id="47721-103">Habilita a recomendação (s) do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="47721-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="47721-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47721-104">SYNTAX</span></span>

### <span data-ttu-id="47721-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="47721-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47721-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47721-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47721-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47721-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47721-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47721-108">DESCRIPTION</span></span>
<span data-ttu-id="47721-109">Este cmdlet habilita uma recomendação que você já eliminou.</span><span class="sxs-lookup"><span data-stu-id="47721-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="47721-110">Você também pode remover todas as supressãos associadas a uma recomendação.</span><span class="sxs-lookup"><span data-stu-id="47721-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="47721-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47721-111">EXAMPLES</span></span>

### <span data-ttu-id="47721-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47721-112">Example 1</span></span>
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

<span data-ttu-id="47721-113">Remove todas as supressões para a recomendação fornecida com o nome "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="47721-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="47721-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47721-114">Example 2</span></span>
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

<span data-ttu-id="47721-115">Remove todas as supressões para a (s) recomendação (s) determinada (s) passada (s) da pipeline.</span><span class="sxs-lookup"><span data-stu-id="47721-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="47721-116">OS</span><span class="sxs-lookup"><span data-stu-id="47721-116">PARAMETERS</span></span>

### <span data-ttu-id="47721-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47721-117">-Confirm</span></span>
<span data-ttu-id="47721-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47721-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47721-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47721-119">-DefaultProfile</span></span>
<span data-ttu-id="47721-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47721-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47721-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47721-121">-InputObject</span></span>
<span data-ttu-id="47721-122">O tipo de objeto do PowerShell PsAzureAdvisorResourceRecommendationBase retornado por Get-AzAdvisorRecommendation chamada.</span><span class="sxs-lookup"><span data-stu-id="47721-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="47721-123">-Recomendaçãoname</span><span class="sxs-lookup"><span data-stu-id="47721-123">-RecommendationName</span></span>
<span data-ttu-id="47721-124">ResourceManager da recomendação.</span><span class="sxs-lookup"><span data-stu-id="47721-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="47721-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47721-125">-ResourceId</span></span>
<span data-ttu-id="47721-126">ID da recomendação a ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="47721-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="47721-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47721-127">-WhatIf</span></span>
<span data-ttu-id="47721-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47721-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47721-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47721-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47721-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47721-130">CommonParameters</span></span>
<span data-ttu-id="47721-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47721-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="47721-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47721-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47721-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47721-133">INPUTS</span></span>

### <span data-ttu-id="47721-134">System. String</span><span class="sxs-lookup"><span data-stu-id="47721-134">System.String</span></span>

### <span data-ttu-id="47721-135">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="47721-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="47721-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47721-136">OUTPUTS</span></span>

### <span data-ttu-id="47721-137">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="47721-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="47721-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47721-138">NOTES</span></span>

## <span data-ttu-id="47721-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47721-139">RELATED LINKS</span></span>
