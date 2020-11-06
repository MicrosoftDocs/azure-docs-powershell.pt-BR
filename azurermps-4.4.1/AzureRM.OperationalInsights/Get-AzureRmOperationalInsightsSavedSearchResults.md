---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433047"
---
# <span data-ttu-id="cf9b9-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="cf9b9-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="cf9b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9b9-103">Retorna os resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf9b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf9b9-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf9b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9b9-106">O cmdlet **Get-AzureRmOperationalInsightsSavedSearchResults** retorna os resultados da consulta especificada pela ID da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="cf9b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="cf9b9-108">Exemplo 1: obter todos os resultados da pesquisa para uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="cf9b9-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="cf9b9-109">Esse comando obtém todos os resultados da pesquisa de uma pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="cf9b9-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf9b9-110">PARAMETERS</span></span>

### <span data-ttu-id="cf9b9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf9b9-111">-ResourceGroupName</span></span>
<span data-ttu-id="cf9b9-112">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="cf9b9-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="cf9b9-113">-SavedSearchId</span></span>
<span data-ttu-id="cf9b9-114">Especifica uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-114">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="cf9b9-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf9b9-115">-WorkspaceName</span></span>
<span data-ttu-id="cf9b9-116">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="cf9b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9b9-117">-DefaultProfile</span></span>
<span data-ttu-id="cf9b9-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9b9-119">CommonParameters</span></span>
<span data-ttu-id="cf9b9-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf9b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9b9-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf9b9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9b9-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf9b9-122">INPUTS</span></span>

## <span data-ttu-id="cf9b9-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf9b9-123">OUTPUTS</span></span>

### <span data-ttu-id="cf9b9-124">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="cf9b9-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="cf9b9-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf9b9-125">NOTES</span></span>

## <span data-ttu-id="cf9b9-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf9b9-126">RELATED LINKS</span></span>

[<span data-ttu-id="cf9b9-127">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="cf9b9-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


