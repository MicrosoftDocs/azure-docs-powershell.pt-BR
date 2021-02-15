---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114881"
---
# <span data-ttu-id="406a5-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="406a5-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="406a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="406a5-102">SYNOPSIS</span></span>
<span data-ttu-id="406a5-103">Obtém uma lista de recomendações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="406a5-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="406a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="406a5-104">SYNTAX</span></span>

### <span data-ttu-id="406a5-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="406a5-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="406a5-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="406a5-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="406a5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="406a5-107">DESCRIPTION</span></span>
<span data-ttu-id="406a5-108">Obtém a lista de recomendações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="406a5-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="406a5-109">Pode ser filtrado por Categoria, ID do recurso, nome etc.</span><span class="sxs-lookup"><span data-stu-id="406a5-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="406a5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="406a5-110">EXAMPLES</span></span>

### <span data-ttu-id="406a5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="406a5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="406a5-112">Obtém a lista de todas as recomendações.</span><span class="sxs-lookup"><span data-stu-id="406a5-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="406a5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="406a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="406a5-114">Obtém a lista de todas as recomendações filtradas por desempenho da categoria.</span><span class="sxs-lookup"><span data-stu-id="406a5-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="406a5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="406a5-115">PARAMETERS</span></span>

### <span data-ttu-id="406a5-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="406a5-116">-Category</span></span>
<span data-ttu-id="406a5-117">Categoria da recomendação</span><span class="sxs-lookup"><span data-stu-id="406a5-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406a5-118">-DefaultProfile</span></span>
<span data-ttu-id="406a5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="406a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="406a5-121">Nome do Grupo de Recursos da recomendação</span><span class="sxs-lookup"><span data-stu-id="406a5-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406a5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="406a5-122">-ResourceId</span></span>
<span data-ttu-id="406a5-123">ResourceId da recomendação</span><span class="sxs-lookup"><span data-stu-id="406a5-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="406a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406a5-124">CommonParameters</span></span>
<span data-ttu-id="406a5-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="406a5-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406a5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406a5-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="406a5-127">INPUTS</span></span>

### <span data-ttu-id="406a5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="406a5-128">System.String</span></span>

## <span data-ttu-id="406a5-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="406a5-129">OUTPUTS</span></span>

### <span data-ttu-id="406a5-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="406a5-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="406a5-131">Notas</span><span class="sxs-lookup"><span data-stu-id="406a5-131">NOTES</span></span>

## <span data-ttu-id="406a5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="406a5-132">RELATED LINKS</span></span>
