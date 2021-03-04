---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 02dded0f03b1ba7bd0936e364b229864e0955022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890204"
---
# <span data-ttu-id="f870e-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f870e-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="f870e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f870e-102">SYNOPSIS</span></span>
<span data-ttu-id="f870e-103">Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870e-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f870e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f870e-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f870e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f870e-105">DESCRIPTION</span></span>
<span data-ttu-id="f870e-106">O cmdlet **Remove-AzOperationalInsightsSavedSearch** remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870e-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f870e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f870e-107">EXAMPLES</span></span>

### <span data-ttu-id="f870e-108">Exemplo 1: Remover uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="f870e-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="f870e-109">Este comando remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870e-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f870e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f870e-110">PARAMETERS</span></span>

### <span data-ttu-id="f870e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f870e-111">-DefaultProfile</span></span>
<span data-ttu-id="f870e-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f870e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f870e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f870e-113">-ResourceGroupName</span></span>
<span data-ttu-id="f870e-114">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870e-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f870e-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f870e-115">-SavedSearchId</span></span>
<span data-ttu-id="f870e-116">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="f870e-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="f870e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f870e-117">-WorkspaceName</span></span>
<span data-ttu-id="f870e-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870e-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f870e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f870e-119">-Confirm</span></span>
<span data-ttu-id="f870e-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f870e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f870e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f870e-121">-WhatIf</span></span>
<span data-ttu-id="f870e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f870e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f870e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f870e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f870e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f870e-124">CommonParameters</span></span>
<span data-ttu-id="f870e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f870e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f870e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f870e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f870e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f870e-127">INPUTS</span></span>

### <span data-ttu-id="f870e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f870e-128">System.String</span></span>

## <span data-ttu-id="f870e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f870e-129">OUTPUTS</span></span>

### <span data-ttu-id="f870e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="f870e-130">System.Void</span></span>

## <span data-ttu-id="f870e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f870e-131">NOTES</span></span>

## <span data-ttu-id="f870e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f870e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f870e-133">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="f870e-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


