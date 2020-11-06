---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601937"
---
# <span data-ttu-id="5c587-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="5c587-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="5c587-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c587-102">SYNOPSIS</span></span>
<span data-ttu-id="5c587-103">Retorna os resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="5c587-103">Returns the results from a query.</span></span>

## <span data-ttu-id="5c587-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c587-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c587-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c587-105">DESCRIPTION</span></span>
<span data-ttu-id="5c587-106">O cmdlet **Get-AzOperationalInsightsSavedSearchResult** retorna os resultados da consulta especificada pela ID da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5c587-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="5c587-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c587-107">EXAMPLES</span></span>

### <span data-ttu-id="5c587-108">Exemplo 1: obter todos os resultados da pesquisa para uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="5c587-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="5c587-109">Esse comando obtém todos os resultados da pesquisa de uma pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5c587-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="5c587-110">OS</span><span class="sxs-lookup"><span data-stu-id="5c587-110">PARAMETERS</span></span>

### <span data-ttu-id="5c587-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c587-111">-DefaultProfile</span></span>
<span data-ttu-id="5c587-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5c587-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c587-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c587-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c587-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c587-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c587-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5c587-115">-SavedSearchId</span></span>
<span data-ttu-id="5c587-116">Especifica uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5c587-116">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c587-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5c587-117">-WorkspaceName</span></span>
<span data-ttu-id="5c587-118">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c587-118">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c587-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c587-119">CommonParameters</span></span>
<span data-ttu-id="5c587-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c587-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c587-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c587-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c587-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c587-122">INPUTS</span></span>

### <span data-ttu-id="5c587-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5c587-123">System.String</span></span>

## <span data-ttu-id="5c587-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c587-124">OUTPUTS</span></span>

### <span data-ttu-id="5c587-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="5c587-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="5c587-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c587-126">NOTES</span></span>

## <span data-ttu-id="5c587-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c587-127">RELATED LINKS</span></span>

[<span data-ttu-id="5c587-128">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="5c587-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


