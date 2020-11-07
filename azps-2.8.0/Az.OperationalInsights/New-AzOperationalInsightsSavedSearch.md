---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7e93042ab376ff0020067a29f9b0642e0ab04de9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784956"
---
# <span data-ttu-id="12c34-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="12c34-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="12c34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12c34-102">SYNOPSIS</span></span>
<span data-ttu-id="12c34-103">Cria uma nova pesquisa salva com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="12c34-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="12c34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12c34-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12c34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12c34-105">DESCRIPTION</span></span>
<span data-ttu-id="12c34-106">O cmdlet **New-AzOperationalInsightsSavedSearch** cria uma nova pesquisa salva com os parâmetros especificados para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="12c34-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="12c34-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12c34-107">EXAMPLES</span></span>

### <span data-ttu-id="12c34-108">Exemplo 1: criar uma nova pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="12c34-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="12c34-109">Esse comando cria uma nova pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="12c34-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="12c34-110">OS</span><span class="sxs-lookup"><span data-stu-id="12c34-110">PARAMETERS</span></span>

### <span data-ttu-id="12c34-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="12c34-111">-Category</span></span>
<span data-ttu-id="12c34-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="12c34-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="12c34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c34-113">-DefaultProfile</span></span>
<span data-ttu-id="12c34-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12c34-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12c34-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="12c34-115">-DisplayName</span></span>
<span data-ttu-id="12c34-116">Especifica o nome de exibição da pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="12c34-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="12c34-117">-Force</span><span class="sxs-lookup"><span data-stu-id="12c34-117">-Force</span></span>
<span data-ttu-id="12c34-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="12c34-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12c34-119">-Consulta</span><span class="sxs-lookup"><span data-stu-id="12c34-119">-Query</span></span>
<span data-ttu-id="12c34-120">Especifica a expressão de consulta para a pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="12c34-120">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="12c34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c34-121">-ResourceGroupName</span></span>
<span data-ttu-id="12c34-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12c34-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="12c34-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="12c34-123">-SavedSearchId</span></span>
<span data-ttu-id="12c34-124">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="12c34-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="12c34-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="12c34-125">-Tag</span></span>
<span data-ttu-id="12c34-126">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="12c34-126">The saved search tags.</span></span>

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

### <span data-ttu-id="12c34-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="12c34-127">-Version</span></span>
<span data-ttu-id="12c34-128">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="12c34-128">Specifies the version.</span></span>

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

### <span data-ttu-id="12c34-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12c34-129">-WorkspaceName</span></span>
<span data-ttu-id="12c34-130">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="12c34-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="12c34-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12c34-131">-Confirm</span></span>
<span data-ttu-id="12c34-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c34-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c34-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c34-133">-WhatIf</span></span>
<span data-ttu-id="12c34-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12c34-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c34-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12c34-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c34-136">CommonParameters</span></span>
<span data-ttu-id="12c34-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c34-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c34-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c34-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12c34-139">INPUTS</span></span>

### <span data-ttu-id="12c34-140">System. String</span><span class="sxs-lookup"><span data-stu-id="12c34-140">System.String</span></span>

### <span data-ttu-id="12c34-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12c34-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="12c34-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="12c34-142">System.Int64</span></span>

## <span data-ttu-id="12c34-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12c34-143">OUTPUTS</span></span>

### <span data-ttu-id="12c34-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="12c34-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="12c34-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12c34-145">NOTES</span></span>

## <span data-ttu-id="12c34-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12c34-146">RELATED LINKS</span></span>

[<span data-ttu-id="12c34-147">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="12c34-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


