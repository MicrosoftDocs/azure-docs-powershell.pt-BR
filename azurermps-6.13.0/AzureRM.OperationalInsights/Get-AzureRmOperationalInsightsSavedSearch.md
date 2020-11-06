---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 712fac06a960eebe546f4554731f69286615b0ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428432"
---
# <span data-ttu-id="1c70e-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1c70e-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1c70e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c70e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c70e-103">Retorna todas as pesquisas salvas de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="1c70e-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c70e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c70e-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c70e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c70e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c70e-106">O cmdlet **Get-AzureRmOperationalInsightsSavedSearch** retorna todas as pesquisas salvas de um espaço de trabalho especificado dentro do grupo de recursos especificado se você não especificar uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="1c70e-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="1c70e-107">Se você especificar uma ID de pesquisa salva, a pesquisa salva correspondente a essa identificação será retornada.</span><span class="sxs-lookup"><span data-stu-id="1c70e-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="1c70e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c70e-108">EXAMPLES</span></span>

### <span data-ttu-id="1c70e-109">Exemplo 1: obter todas as pesquisas salvas para um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1c70e-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="1c70e-110">Esse comando obtém todos os recursos salvos associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1c70e-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="1c70e-111">Exemplo 2: obter uma pesquisa salva específica por ID</span><span class="sxs-lookup"><span data-stu-id="1c70e-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="1c70e-112">Esse comando obtém uma pesquisa salva específica por sua identificação.</span><span class="sxs-lookup"><span data-stu-id="1c70e-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="1c70e-113">OS</span><span class="sxs-lookup"><span data-stu-id="1c70e-113">PARAMETERS</span></span>

### <span data-ttu-id="1c70e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c70e-114">-DefaultProfile</span></span>
<span data-ttu-id="1c70e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1c70e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c70e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c70e-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c70e-117">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1c70e-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="1c70e-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1c70e-118">-SavedSearchId</span></span>
<span data-ttu-id="1c70e-119">Especifica uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="1c70e-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c70e-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c70e-120">-WorkspaceName</span></span>
<span data-ttu-id="1c70e-121">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1c70e-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="1c70e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c70e-122">CommonParameters</span></span>
<span data-ttu-id="1c70e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c70e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c70e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c70e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c70e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c70e-125">INPUTS</span></span>

### <span data-ttu-id="1c70e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c70e-126">System.String</span></span>

## <span data-ttu-id="1c70e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c70e-127">OUTPUTS</span></span>

### <span data-ttu-id="1c70e-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="1c70e-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="1c70e-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="1c70e-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="1c70e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c70e-130">NOTES</span></span>

## <span data-ttu-id="1c70e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c70e-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c70e-132">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="1c70e-132">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


