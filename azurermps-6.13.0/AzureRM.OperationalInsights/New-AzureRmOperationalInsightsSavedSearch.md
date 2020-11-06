---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 247589f50028fb8d4cebf78f0ad45bb2124e43cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429402"
---
# <span data-ttu-id="5e1c6-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="5e1c6-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="5e1c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1c6-103">Cria uma nova pesquisa salva com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e1c6-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e1c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e1c6-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1c6-106">O cmdlet **New-AzureRmOperationalInsightsSavedSearch** cria uma nova pesquisa salva com os parâmetros especificados para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="5e1c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e1c6-107">EXAMPLES</span></span>

### <span data-ttu-id="5e1c6-108">Exemplo 1: criar uma nova pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="5e1c6-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="5e1c6-109">Esse comando cria uma nova pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="5e1c6-110">OS</span><span class="sxs-lookup"><span data-stu-id="5e1c6-110">PARAMETERS</span></span>

### <span data-ttu-id="5e1c6-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="5e1c6-111">-Category</span></span>
<span data-ttu-id="5e1c6-112">Especifica o nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="5e1c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1c6-113">-DefaultProfile</span></span>
<span data-ttu-id="5e1c6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e1c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e1c6-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e1c6-115">-DisplayName</span></span>
<span data-ttu-id="5e1c6-116">Especifica o nome de exibição da pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="5e1c6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5e1c6-117">-Force</span></span>
<span data-ttu-id="5e1c6-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e1c6-119">-Consulta</span><span class="sxs-lookup"><span data-stu-id="5e1c6-119">-Query</span></span>
<span data-ttu-id="5e1c6-120">Especifica o nome da consulta.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="5e1c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e1c6-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="5e1c6-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5e1c6-123">-SavedSearchId</span></span>
<span data-ttu-id="5e1c6-124">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="5e1c6-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="5e1c6-125">-Tag</span></span>
<span data-ttu-id="5e1c6-126">As marcas de pesquisa salvas.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-126">The saved search tags.</span></span>

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

### <span data-ttu-id="5e1c6-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="5e1c6-127">-Version</span></span>
<span data-ttu-id="5e1c6-128">Especifica a versão.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-128">Specifies the version.</span></span>

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

### <span data-ttu-id="5e1c6-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5e1c6-129">-WorkspaceName</span></span>
<span data-ttu-id="5e1c6-130">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="5e1c6-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e1c6-131">-Confirm</span></span>
<span data-ttu-id="5e1c6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1c6-133">-WhatIf</span></span>
<span data-ttu-id="5e1c6-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1c6-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1c6-136">CommonParameters</span></span>
<span data-ttu-id="5e1c6-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1c6-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1c6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1c6-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e1c6-139">INPUTS</span></span>

### <span data-ttu-id="5e1c6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5e1c6-140">System.String</span></span>

### <span data-ttu-id="5e1c6-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e1c6-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5e1c6-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="5e1c6-142">System.Int64</span></span>

## <span data-ttu-id="5e1c6-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e1c6-143">OUTPUTS</span></span>

### <span data-ttu-id="5e1c6-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="5e1c6-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="5e1c6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e1c6-145">NOTES</span></span>

## <span data-ttu-id="5e1c6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e1c6-146">RELATED LINKS</span></span>

[<span data-ttu-id="5e1c6-147">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="5e1c6-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


