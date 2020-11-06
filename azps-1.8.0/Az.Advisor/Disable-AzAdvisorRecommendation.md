---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595763"
---
# <span data-ttu-id="40d3d-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="40d3d-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="40d3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="40d3d-103">Desabilitar uma recomendação do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="40d3d-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="40d3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40d3d-104">SYNTAX</span></span>

### <span data-ttu-id="40d3d-105">IdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="40d3d-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d3d-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d3d-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d3d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d3d-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="40d3d-109">Cria uma supressão para recomendação (s), isso permite que uma determinada recomendação seja adiada por uma duração específica ou infinitamente.</span><span class="sxs-lookup"><span data-stu-id="40d3d-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="40d3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40d3d-110">EXAMPLES</span></span>

### <span data-ttu-id="40d3d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40d3d-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="40d3d-112">Crie uma supressão para o nome de recomendação fornecido com um padrão-SuppressionName e padrão os dias como-1.</span><span class="sxs-lookup"><span data-stu-id="40d3d-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="40d3d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="40d3d-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="40d3d-114">Uma supressão é criada para a identificação de recomendação fornecida.</span><span class="sxs-lookup"><span data-stu-id="40d3d-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="40d3d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="40d3d-115">Example 3</span></span>
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

<span data-ttu-id="40d3d-116">Criação de uma supressão, tubulação de Get-AzAdvisorRecommendation para Disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="40d3d-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="40d3d-117">OS</span><span class="sxs-lookup"><span data-stu-id="40d3d-117">PARAMETERS</span></span>

### <span data-ttu-id="40d3d-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40d3d-118">-Confirm</span></span>
<span data-ttu-id="40d3d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d3d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d3d-120">-Dias</span><span class="sxs-lookup"><span data-stu-id="40d3d-120">-Days</span></span>
<span data-ttu-id="40d3d-121">Dias para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="40d3d-121">Days to disable.</span></span>

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

### <span data-ttu-id="40d3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d3d-122">-DefaultProfile</span></span>
<span data-ttu-id="40d3d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40d3d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d3d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40d3d-124">-InputObject</span></span>
<span data-ttu-id="40d3d-125">O tipo de objeto do PowerShell PsAzureAdvisorResourceRecommendationBase retornado por Get-AzAdvisorRecommendation chamada.</span><span class="sxs-lookup"><span data-stu-id="40d3d-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="40d3d-126">-Recomendaçãoname</span><span class="sxs-lookup"><span data-stu-id="40d3d-126">-RecommendationName</span></span>
<span data-ttu-id="40d3d-127">ResourceManager da recomendação</span><span class="sxs-lookup"><span data-stu-id="40d3d-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="40d3d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40d3d-128">-ResourceId</span></span>
<span data-ttu-id="40d3d-129">ID da recomendação a ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="40d3d-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="40d3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d3d-130">-WhatIf</span></span>
<span data-ttu-id="40d3d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40d3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d3d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40d3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d3d-133">CommonParameters</span></span>
<span data-ttu-id="40d3d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="40d3d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d3d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d3d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40d3d-136">INPUTS</span></span>

### <span data-ttu-id="40d3d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="40d3d-137">System.String</span></span>

### <span data-ttu-id="40d3d-138">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="40d3d-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="40d3d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40d3d-139">OUTPUTS</span></span>

### <span data-ttu-id="40d3d-140">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="40d3d-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="40d3d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40d3d-141">NOTES</span></span>

## <span data-ttu-id="40d3d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40d3d-142">RELATED LINKS</span></span>
