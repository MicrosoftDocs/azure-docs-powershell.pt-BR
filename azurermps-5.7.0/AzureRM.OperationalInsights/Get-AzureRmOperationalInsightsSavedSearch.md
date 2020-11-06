---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428850"
---
# <span data-ttu-id="5d280-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="5d280-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="5d280-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d280-102">SYNOPSIS</span></span>
<span data-ttu-id="5d280-103">Retorna todas as pesquisas salvas de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="5d280-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d280-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d280-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d280-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d280-105">DESCRIPTION</span></span>
<span data-ttu-id="5d280-106">O cmdlet **Get-AzureRmOperationalInsightsSavedSearch** retorna todas as pesquisas salvas de um espaço de trabalho especificado dentro do grupo de recursos especificado se você não especificar uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5d280-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="5d280-107">Se você especificar uma ID de pesquisa salva, a pesquisa salva correspondente a essa identificação será retornada.</span><span class="sxs-lookup"><span data-stu-id="5d280-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="5d280-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d280-108">EXAMPLES</span></span>

### <span data-ttu-id="5d280-109">Exemplo 1: obter todas as pesquisas salvas para um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5d280-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="5d280-110">Esse comando obtém todos os recursos salvos associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d280-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="5d280-111">Exemplo 2: obter uma pesquisa salva específica por ID</span><span class="sxs-lookup"><span data-stu-id="5d280-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="5d280-112">Esse comando obtém uma pesquisa salva específica por sua identificação.</span><span class="sxs-lookup"><span data-stu-id="5d280-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="5d280-113">OS</span><span class="sxs-lookup"><span data-stu-id="5d280-113">PARAMETERS</span></span>

### <span data-ttu-id="5d280-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d280-114">-DefaultProfile</span></span>
<span data-ttu-id="5d280-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5d280-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d280-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d280-116">-ResourceGroupName</span></span>
<span data-ttu-id="5d280-117">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d280-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d280-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5d280-118">-SavedSearchId</span></span>
<span data-ttu-id="5d280-119">Especifica uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5d280-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d280-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d280-120">-WorkspaceName</span></span>
<span data-ttu-id="5d280-121">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d280-121">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d280-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d280-122">CommonParameters</span></span>
<span data-ttu-id="5d280-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d280-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d280-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d280-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d280-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d280-125">INPUTS</span></span>

### <span data-ttu-id="5d280-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5d280-126">None</span></span>
<span data-ttu-id="5d280-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5d280-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d280-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d280-128">OUTPUTS</span></span>

### <span data-ttu-id="5d280-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="5d280-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="5d280-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="5d280-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="5d280-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d280-131">NOTES</span></span>

## <span data-ttu-id="5d280-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d280-132">RELATED LINKS</span></span>

[<span data-ttu-id="5d280-133">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="5d280-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


