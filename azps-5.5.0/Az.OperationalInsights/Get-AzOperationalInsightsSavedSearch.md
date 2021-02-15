---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111526"
---
# <span data-ttu-id="c9ca4-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c9ca4-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c9ca4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ca4-103">Retorna todas as pesquisas salvas para um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="c9ca4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9ca4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ca4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ca4-106">O cmdlet **Get-AzOperationalInsightsSavedSearch** retorna todas as pesquisas salvas para um espaço de trabalho especificado no grupo de recursos especificado se você não especificar uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="c9ca4-107">Se você especificar uma ID de pesquisa salva, a pesquisa salva correspondente a essa ID será retornada.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="c9ca4-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9ca4-108">EXAMPLES</span></span>

### <span data-ttu-id="c9ca4-109">Exemplo 1: Obter todas as pesquisas salvas de um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c9ca4-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c9ca4-110">Esse comando obtém todos os recursos salvos associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="c9ca4-111">Exemplo 2: Obter uma pesquisa salva específica por ID</span><span class="sxs-lookup"><span data-stu-id="c9ca4-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="c9ca4-112">Esse comando obtém uma pesquisa salva específica por sua ID.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="c9ca4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9ca4-113">PARAMETERS</span></span>

### <span data-ttu-id="c9ca4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ca4-114">-DefaultProfile</span></span>
<span data-ttu-id="c9ca4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c9ca4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9ca4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ca4-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9ca4-117">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c9ca4-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c9ca4-118">-SavedSearchId</span></span>
<span data-ttu-id="c9ca4-119">Especifica uma ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="c9ca4-120">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c9ca4-120">-WorkspaceName</span></span>
<span data-ttu-id="c9ca4-121">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c9ca4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ca4-122">CommonParameters</span></span>
<span data-ttu-id="c9ca4-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ca4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ca4-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ca4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ca4-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9ca4-125">INPUTS</span></span>

### <span data-ttu-id="c9ca4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c9ca4-126">System.String</span></span>

## <span data-ttu-id="c9ca4-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9ca4-127">OUTPUTS</span></span>

### <span data-ttu-id="c9ca4-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9ca4-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="c9ca4-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="c9ca4-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="c9ca4-130">Notas</span><span class="sxs-lookup"><span data-stu-id="c9ca4-130">NOTES</span></span>

## <span data-ttu-id="c9ca4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9ca4-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9ca4-132">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="c9ca4-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


