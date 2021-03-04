---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890223"
---
# <span data-ttu-id="0297f-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="0297f-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="0297f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0297f-102">SYNOPSIS</span></span>
<span data-ttu-id="0297f-103">Cria uma nova pesquisa salva com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="0297f-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="0297f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0297f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0297f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0297f-105">DESCRIPTION</span></span>
<span data-ttu-id="0297f-106">O cmdlet **New-AzOperationalInsightsSavedSearch** cria uma nova pesquisa salva com os parâmetros especificados para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0297f-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="0297f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0297f-107">EXAMPLES</span></span>

### <span data-ttu-id="0297f-108">Exemplo 1: Criar uma nova pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="0297f-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="0297f-109">Este comando cria uma nova pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="0297f-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="0297f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0297f-110">PARAMETERS</span></span>

### <span data-ttu-id="0297f-111">-Category</span><span class="sxs-lookup"><span data-stu-id="0297f-111">-Category</span></span>
<span data-ttu-id="0297f-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="0297f-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="0297f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0297f-113">-DefaultProfile</span></span>
<span data-ttu-id="0297f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0297f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0297f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0297f-115">-DisplayName</span></span>
<span data-ttu-id="0297f-116">Especifica o nome de exibição de pesquisa salvo.</span><span class="sxs-lookup"><span data-stu-id="0297f-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="0297f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0297f-117">-Force</span></span>
<span data-ttu-id="0297f-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0297f-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0297f-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="0297f-119">-FunctionAlias</span></span>
<span data-ttu-id="0297f-120">O alias da função se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="0297f-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0297f-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="0297f-121">-FunctionParameter</span></span>
<span data-ttu-id="0297f-122">Os parâmetros de função opcionais se a consulta servir como uma função.</span><span class="sxs-lookup"><span data-stu-id="0297f-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="0297f-123">O valor deve estar no seguinte formato: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="0297f-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="0297f-124">Para obter mais exemplos e sintaxe adequada, consulte https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="0297f-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0297f-125">-Query</span><span class="sxs-lookup"><span data-stu-id="0297f-125">-Query</span></span>
<span data-ttu-id="0297f-126">Especifica a expressão de consulta da pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="0297f-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="0297f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0297f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0297f-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0297f-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="0297f-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="0297f-129">-SavedSearchId</span></span>
<span data-ttu-id="0297f-130">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="0297f-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="0297f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0297f-131">-Tag</span></span>
<span data-ttu-id="0297f-132">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="0297f-132">The saved search tags.</span></span>

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

### <span data-ttu-id="0297f-133">-Version</span><span class="sxs-lookup"><span data-stu-id="0297f-133">-Version</span></span>
<span data-ttu-id="0297f-134">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="0297f-134">Specifies the version.</span></span>

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

### <span data-ttu-id="0297f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0297f-135">-WorkspaceName</span></span>
<span data-ttu-id="0297f-136">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0297f-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0297f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0297f-137">-Confirm</span></span>
<span data-ttu-id="0297f-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0297f-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0297f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0297f-139">-WhatIf</span></span>
<span data-ttu-id="0297f-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0297f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0297f-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0297f-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0297f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0297f-142">CommonParameters</span></span>
<span data-ttu-id="0297f-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0297f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0297f-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0297f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0297f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0297f-145">INPUTS</span></span>

### <span data-ttu-id="0297f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0297f-146">System.String</span></span>

### <span data-ttu-id="0297f-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0297f-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0297f-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="0297f-148">System.Int64</span></span>

## <span data-ttu-id="0297f-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0297f-149">OUTPUTS</span></span>

### <span data-ttu-id="0297f-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="0297f-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="0297f-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="0297f-151">NOTES</span></span>

## <span data-ttu-id="0297f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0297f-152">RELATED LINKS</span></span>

[<span data-ttu-id="0297f-153">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="0297f-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


