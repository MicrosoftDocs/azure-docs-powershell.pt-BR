---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 3695ee9d027733d3adea17797ffbcf669136e66b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887267"
---
# <span data-ttu-id="6651c-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="6651c-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="6651c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6651c-102">SYNOPSIS</span></span>
<span data-ttu-id="6651c-103">Desabilite uma recomendação do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="6651c-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="6651c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6651c-104">SYNTAX</span></span>

### <span data-ttu-id="6651c-105">IdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6651c-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6651c-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6651c-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6651c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6651c-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6651c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6651c-108">DESCRIPTION</span></span>
<span data-ttu-id="6651c-109">Cria uma supressão para recomendações, isso permite que uma recomendação específica seja adiada por uma duração específica ou infinitamente.</span><span class="sxs-lookup"><span data-stu-id="6651c-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="6651c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6651c-110">EXAMPLES</span></span>

### <span data-ttu-id="6651c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6651c-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="6651c-112">Crie uma supressão para o nome de recomendação determinado com um padrão-SuppressionName e dias padrão como -1.</span><span class="sxs-lookup"><span data-stu-id="6651c-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="6651c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6651c-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="6651c-114">Uma supressão é criada para a ID de recomendação determinada.</span><span class="sxs-lookup"><span data-stu-id="6651c-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="6651c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6651c-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="6651c-116">Criando uma supressão, canalização de Get-AzAdvisorRecommendation para Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="6651c-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="6651c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6651c-117">PARAMETERS</span></span>

### <span data-ttu-id="6651c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6651c-118">-Confirm</span></span>
<span data-ttu-id="6651c-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6651c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6651c-120">-Days</span><span class="sxs-lookup"><span data-stu-id="6651c-120">-Days</span></span>
<span data-ttu-id="6651c-121">Dias para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="6651c-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6651c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6651c-122">-DefaultProfile</span></span>
<span data-ttu-id="6651c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6651c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6651c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6651c-124">-InputObject</span></span>
<span data-ttu-id="6651c-125">O tipo de objeto do powershell PsAzureAdvisorResourceRecommendationBase retornado por Get-AzAdvisorRecommendation chamada.</span><span class="sxs-lookup"><span data-stu-id="6651c-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="6651c-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="6651c-126">-RecommendationName</span></span>
<span data-ttu-id="6651c-127">ResourceName da recomendação</span><span class="sxs-lookup"><span data-stu-id="6651c-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="6651c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6651c-128">-ResourceId</span></span>
<span data-ttu-id="6651c-129">ID da recomendação a ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="6651c-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6651c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6651c-130">-WhatIf</span></span>
<span data-ttu-id="6651c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6651c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6651c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6651c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6651c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6651c-133">CommonParameters</span></span>
<span data-ttu-id="6651c-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6651c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6651c-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6651c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6651c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6651c-136">INPUTS</span></span>

### <span data-ttu-id="6651c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6651c-137">System.String</span></span>

### <span data-ttu-id="6651c-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="6651c-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="6651c-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6651c-139">OUTPUTS</span></span>

### <span data-ttu-id="6651c-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="6651c-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="6651c-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="6651c-141">NOTES</span></span>

## <span data-ttu-id="6651c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6651c-142">RELATED LINKS</span></span>
