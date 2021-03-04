---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 25d973d6a568695fbca7371b229cf9bb18fcd5cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890196"
---
# <span data-ttu-id="80949-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="80949-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="80949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80949-102">SYNOPSIS</span></span>
<span data-ttu-id="80949-103">Atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="80949-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="80949-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80949-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80949-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80949-105">DESCRIPTION</span></span>
<span data-ttu-id="80949-106">O cmdlet **Set-AzOperationalInsightsSavedSearch** atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="80949-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="80949-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80949-107">EXAMPLES</span></span>

### <span data-ttu-id="80949-108">Exemplo 1: define uma pesquisa salva com propriedades atualizadas</span><span class="sxs-lookup"><span data-stu-id="80949-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="80949-109">Este comando define uma pesquisa salva com propriedades atualizadas.</span><span class="sxs-lookup"><span data-stu-id="80949-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="80949-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80949-110">PARAMETERS</span></span>

### <span data-ttu-id="80949-111">-Category</span><span class="sxs-lookup"><span data-stu-id="80949-111">-Category</span></span>
<span data-ttu-id="80949-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="80949-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80949-113">-DefaultProfile</span></span>
<span data-ttu-id="80949-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="80949-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80949-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="80949-115">-DisplayName</span></span>
<span data-ttu-id="80949-116">Especifica o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="80949-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="80949-117">-ETag</span></span>
<span data-ttu-id="80949-118">Especifica o nome ETag.</span><span class="sxs-lookup"><span data-stu-id="80949-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="80949-119">-FunctionAlias</span></span>
<span data-ttu-id="80949-120">O alias da função se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="80949-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80949-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="80949-121">-FunctionParameter</span></span>
<span data-ttu-id="80949-122">Os parâmetros de função opcionais se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="80949-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="80949-123">O valor deve estar no seguinte formato: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="80949-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="80949-124">Para obter mais exemplos e sintaxe adequada, consulte https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="80949-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80949-125">-Query</span><span class="sxs-lookup"><span data-stu-id="80949-125">-Query</span></span>
<span data-ttu-id="80949-126">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="80949-126">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80949-127">-ResourceGroupName</span></span>
<span data-ttu-id="80949-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="80949-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="80949-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="80949-129">-SavedSearchId</span></span>
<span data-ttu-id="80949-130">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="80949-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="80949-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="80949-131">-Tag</span></span>
<span data-ttu-id="80949-132">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="80949-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-133">-Version</span><span class="sxs-lookup"><span data-stu-id="80949-133">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80949-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80949-134">-WorkspaceName</span></span>
<span data-ttu-id="80949-135">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="80949-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="80949-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80949-136">CommonParameters</span></span>
<span data-ttu-id="80949-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80949-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80949-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80949-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80949-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80949-139">INPUTS</span></span>

### <span data-ttu-id="80949-140">System.String</span><span class="sxs-lookup"><span data-stu-id="80949-140">System.String</span></span>

### <span data-ttu-id="80949-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="80949-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="80949-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="80949-142">System.Int64</span></span>

## <span data-ttu-id="80949-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80949-143">OUTPUTS</span></span>

### <span data-ttu-id="80949-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="80949-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="80949-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="80949-145">NOTES</span></span>

## <span data-ttu-id="80949-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80949-146">RELATED LINKS</span></span>

[<span data-ttu-id="80949-147">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="80949-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


