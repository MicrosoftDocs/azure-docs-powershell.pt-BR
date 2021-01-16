---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271663"
---
# <span data-ttu-id="d282b-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d282b-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="d282b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d282b-102">SYNOPSIS</span></span>
<span data-ttu-id="d282b-103">Atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="d282b-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="d282b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d282b-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d282b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d282b-105">DESCRIPTION</span></span>
<span data-ttu-id="d282b-106">O cmdlet **set-AzOperationalInsightsSavedSearch** atualiza uma pesquisa salva que já existe.</span><span class="sxs-lookup"><span data-stu-id="d282b-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="d282b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d282b-107">EXAMPLES</span></span>

### <span data-ttu-id="d282b-108">Exemplo 1: define uma pesquisa salva com propriedades atualizadas</span><span class="sxs-lookup"><span data-stu-id="d282b-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="d282b-109">Este comando define uma pesquisa salva com propriedades atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d282b-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="d282b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d282b-110">PARAMETERS</span></span>

### <span data-ttu-id="d282b-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="d282b-111">-Category</span></span>
<span data-ttu-id="d282b-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="d282b-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="d282b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d282b-113">-DefaultProfile</span></span>
<span data-ttu-id="d282b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d282b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d282b-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d282b-115">-DisplayName</span></span>
<span data-ttu-id="d282b-116">Especifica o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="d282b-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="d282b-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="d282b-117">-ETag</span></span>
<span data-ttu-id="d282b-118">Especifica o nome ETag.</span><span class="sxs-lookup"><span data-stu-id="d282b-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="d282b-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="d282b-119">-FunctionAlias</span></span>
<span data-ttu-id="d282b-120">O alias da função se Query funciona como uma função.</span><span class="sxs-lookup"><span data-stu-id="d282b-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="d282b-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="d282b-121">-FunctionParameter</span></span>
<span data-ttu-id="d282b-122">Os parâmetros da função opcional se Query funcionar como uma função.</span><span class="sxs-lookup"><span data-stu-id="d282b-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="d282b-123">O valor deve estar no seguinte formato: ' param-Nome1: type1 = default_value1, param-nome2: type2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="d282b-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="d282b-124">Para obter mais exemplos e sintaxe apropriada, consulte https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="d282b-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="d282b-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d282b-125">-Query</span></span>
<span data-ttu-id="d282b-126">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="d282b-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="d282b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d282b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d282b-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d282b-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="d282b-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d282b-129">-SavedSearchId</span></span>
<span data-ttu-id="d282b-130">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="d282b-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="d282b-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="d282b-131">-Tag</span></span>
<span data-ttu-id="d282b-132">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="d282b-132">The saved search tags.</span></span>

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

### <span data-ttu-id="d282b-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="d282b-133">-Version</span></span>
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

### <span data-ttu-id="d282b-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d282b-134">-WorkspaceName</span></span>
<span data-ttu-id="d282b-135">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d282b-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d282b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d282b-136">CommonParameters</span></span>
<span data-ttu-id="d282b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d282b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d282b-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d282b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d282b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d282b-139">INPUTS</span></span>

### <span data-ttu-id="d282b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d282b-140">System.String</span></span>

### <span data-ttu-id="d282b-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d282b-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d282b-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="d282b-142">System.Int64</span></span>

## <span data-ttu-id="d282b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d282b-143">OUTPUTS</span></span>

### <span data-ttu-id="d282b-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="d282b-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="d282b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d282b-145">NOTES</span></span>

## <span data-ttu-id="d282b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d282b-146">RELATED LINKS</span></span>

[<span data-ttu-id="d282b-147">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="d282b-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


