---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114066"
---
# <span data-ttu-id="d4359-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d4359-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="d4359-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4359-102">SYNOPSIS</span></span>
<span data-ttu-id="d4359-103">Atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="d4359-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="d4359-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4359-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4359-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4359-105">DESCRIPTION</span></span>
<span data-ttu-id="d4359-106">O cmdlet **Set-AzOperationalInsightsSavedSearch** atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="d4359-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="d4359-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4359-107">EXAMPLES</span></span>

### <span data-ttu-id="d4359-108">Exemplo 1: define uma pesquisa salva com propriedades atualizadas</span><span class="sxs-lookup"><span data-stu-id="d4359-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="d4359-109">Esse comando define uma pesquisa salva com propriedades atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d4359-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="d4359-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4359-110">PARAMETERS</span></span>

### <span data-ttu-id="d4359-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="d4359-111">-Category</span></span>
<span data-ttu-id="d4359-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="d4359-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="d4359-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4359-113">-DefaultProfile</span></span>
<span data-ttu-id="d4359-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d4359-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4359-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d4359-115">-DisplayName</span></span>
<span data-ttu-id="d4359-116">Especifica o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="d4359-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="d4359-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="d4359-117">-ETag</span></span>
<span data-ttu-id="d4359-118">Especifica o nome de ETag.</span><span class="sxs-lookup"><span data-stu-id="d4359-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="d4359-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="d4359-119">-FunctionAlias</span></span>
<span data-ttu-id="d4359-120">O alias da função se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="d4359-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="d4359-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="d4359-121">-FunctionParameter</span></span>
<span data-ttu-id="d4359-122">Os parâmetros de função opcionais se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="d4359-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="d4359-123">O valor deve estar no seguinte formato: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="d4359-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="d4359-124">Para obter mais exemplos e sintaxe adequada, consulte https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="d4359-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="d4359-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d4359-125">-Query</span></span>
<span data-ttu-id="d4359-126">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="d4359-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="d4359-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4359-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4359-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4359-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="d4359-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d4359-129">-SavedSearchId</span></span>
<span data-ttu-id="d4359-130">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="d4359-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="d4359-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4359-131">-Tag</span></span>
<span data-ttu-id="d4359-132">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="d4359-132">The saved search tags.</span></span>

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

### <span data-ttu-id="d4359-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="d4359-133">-Version</span></span>
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

### <span data-ttu-id="d4359-134">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d4359-134">-WorkspaceName</span></span>
<span data-ttu-id="d4359-135">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d4359-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d4359-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4359-136">CommonParameters</span></span>
<span data-ttu-id="d4359-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4359-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4359-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4359-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4359-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d4359-139">INPUTS</span></span>

### <span data-ttu-id="d4359-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d4359-140">System.String</span></span>

### <span data-ttu-id="d4359-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4359-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d4359-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="d4359-142">System.Int64</span></span>

## <span data-ttu-id="d4359-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d4359-143">OUTPUTS</span></span>

### <span data-ttu-id="d4359-144">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="d4359-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="d4359-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d4359-145">NOTES</span></span>

## <span data-ttu-id="d4359-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4359-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4359-147">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="d4359-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


