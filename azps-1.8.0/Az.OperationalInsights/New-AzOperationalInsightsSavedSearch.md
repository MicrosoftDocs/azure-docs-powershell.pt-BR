---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601922"
---
# <span data-ttu-id="a045c-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a045c-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a045c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a045c-102">SYNOPSIS</span></span>
<span data-ttu-id="a045c-103">Cria uma nova pesquisa salva com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="a045c-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="a045c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a045c-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a045c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a045c-105">DESCRIPTION</span></span>
<span data-ttu-id="a045c-106">O cmdlet **New-AzOperationalInsightsSavedSearch** cria uma nova pesquisa salva com os parâmetros especificados para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a045c-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="a045c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a045c-107">EXAMPLES</span></span>

### <span data-ttu-id="a045c-108">Exemplo 1: criar uma nova pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="a045c-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="a045c-109">Esse comando cria uma nova pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="a045c-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="a045c-110">OS</span><span class="sxs-lookup"><span data-stu-id="a045c-110">PARAMETERS</span></span>

### <span data-ttu-id="a045c-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="a045c-111">-Category</span></span>
<span data-ttu-id="a045c-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="a045c-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="a045c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a045c-113">-DefaultProfile</span></span>
<span data-ttu-id="a045c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a045c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a045c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a045c-115">-DisplayName</span></span>
<span data-ttu-id="a045c-116">Especifica o nome de exibição da pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="a045c-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="a045c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a045c-117">-Force</span></span>
<span data-ttu-id="a045c-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a045c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a045c-119">-Consulta</span><span class="sxs-lookup"><span data-stu-id="a045c-119">-Query</span></span>
<span data-ttu-id="a045c-120">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="a045c-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="a045c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a045c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a045c-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a045c-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="a045c-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a045c-123">-SavedSearchId</span></span>
<span data-ttu-id="a045c-124">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="a045c-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="a045c-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="a045c-125">-Tag</span></span>
<span data-ttu-id="a045c-126">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="a045c-126">The saved search tags.</span></span>

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

### <span data-ttu-id="a045c-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="a045c-127">-Version</span></span>
<span data-ttu-id="a045c-128">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="a045c-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a045c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a045c-129">-WorkspaceName</span></span>
<span data-ttu-id="a045c-130">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a045c-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a045c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a045c-131">-Confirm</span></span>
<span data-ttu-id="a045c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a045c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a045c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a045c-133">-WhatIf</span></span>
<span data-ttu-id="a045c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a045c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a045c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a045c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a045c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a045c-136">CommonParameters</span></span>
<span data-ttu-id="a045c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a045c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a045c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a045c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a045c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a045c-139">INPUTS</span></span>

### <span data-ttu-id="a045c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a045c-140">System.String</span></span>

### <span data-ttu-id="a045c-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a045c-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a045c-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="a045c-142">System.Int64</span></span>

## <span data-ttu-id="a045c-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a045c-143">OUTPUTS</span></span>

### <span data-ttu-id="a045c-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="a045c-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="a045c-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a045c-145">NOTES</span></span>

## <span data-ttu-id="a045c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a045c-146">RELATED LINKS</span></span>

[<span data-ttu-id="a045c-147">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="a045c-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


