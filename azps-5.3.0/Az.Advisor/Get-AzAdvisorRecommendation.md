---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432816"
---
# <span data-ttu-id="dbd65-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="dbd65-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="dbd65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbd65-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd65-103">Obtém uma lista de recomendações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="dbd65-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="dbd65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbd65-104">SYNTAX</span></span>

### <span data-ttu-id="dbd65-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dbd65-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbd65-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbd65-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd65-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbd65-107">DESCRIPTION</span></span>
<span data-ttu-id="dbd65-108">Obtém a lista de recomendações do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="dbd65-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="dbd65-109">Pode ser filtrado por categoria, ID de recurso, nome etc.</span><span class="sxs-lookup"><span data-stu-id="dbd65-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="dbd65-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbd65-110">EXAMPLES</span></span>

### <span data-ttu-id="dbd65-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dbd65-111">Example 1</span></span>
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
<span data-ttu-id="dbd65-112">Obtém a lista de todas as recomendações.</span><span class="sxs-lookup"><span data-stu-id="dbd65-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="dbd65-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dbd65-113">Example 2</span></span>
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
<span data-ttu-id="dbd65-114">Obtém a lista de todas as recomendações filtradas pelo desempenho da categoria.</span><span class="sxs-lookup"><span data-stu-id="dbd65-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="dbd65-115">OS</span><span class="sxs-lookup"><span data-stu-id="dbd65-115">PARAMETERS</span></span>

### <span data-ttu-id="dbd65-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="dbd65-116">-Category</span></span>
<span data-ttu-id="dbd65-117">Categoria da recomendação</span><span class="sxs-lookup"><span data-stu-id="dbd65-117">Category of the recommendation</span></span>

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

### <span data-ttu-id="dbd65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd65-118">-DefaultProfile</span></span>
<span data-ttu-id="dbd65-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd65-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd65-120">-ResourceGroupName</span></span>
<span data-ttu-id="dbd65-121">Nome do o nome do botão de Resource da recomendação</span><span class="sxs-lookup"><span data-stu-id="dbd65-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="dbd65-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd65-122">-ResourceId</span></span>
<span data-ttu-id="dbd65-123">ResourceId da recomendação</span><span class="sxs-lookup"><span data-stu-id="dbd65-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="dbd65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd65-124">CommonParameters</span></span>
<span data-ttu-id="dbd65-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dbd65-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd65-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd65-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbd65-127">INPUTS</span></span>

### <span data-ttu-id="dbd65-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd65-128">System.String</span></span>

## <span data-ttu-id="dbd65-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbd65-129">OUTPUTS</span></span>

### <span data-ttu-id="dbd65-130">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="dbd65-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="dbd65-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbd65-131">NOTES</span></span>

## <span data-ttu-id="dbd65-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbd65-132">RELATED LINKS</span></span>
