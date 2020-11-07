---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 931c85b649393d33f03e778d0e34cf6644e4c2d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947289"
---
# <span data-ttu-id="49f2c-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="49f2c-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="49f2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="49f2c-103">Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="49f2c-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="49f2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49f2c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f2c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="49f2c-106">O cmdlet **Remove-AzOperationalInsightsSavedSearch** remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="49f2c-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="49f2c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49f2c-107">EXAMPLES</span></span>

### <span data-ttu-id="49f2c-108">Exemplo 1: remover uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="49f2c-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="49f2c-109">Esse comando Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="49f2c-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="49f2c-110">OS</span><span class="sxs-lookup"><span data-stu-id="49f2c-110">PARAMETERS</span></span>

### <span data-ttu-id="49f2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f2c-111">-DefaultProfile</span></span>
<span data-ttu-id="49f2c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49f2c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49f2c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f2c-113">-ResourceGroupName</span></span>
<span data-ttu-id="49f2c-114">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="49f2c-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="49f2c-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="49f2c-115">-SavedSearchId</span></span>
<span data-ttu-id="49f2c-116">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="49f2c-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="49f2c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49f2c-117">-WorkspaceName</span></span>
<span data-ttu-id="49f2c-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="49f2c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="49f2c-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49f2c-119">-Confirm</span></span>
<span data-ttu-id="49f2c-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f2c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f2c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f2c-121">-WhatIf</span></span>
<span data-ttu-id="49f2c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49f2c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f2c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49f2c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f2c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f2c-124">CommonParameters</span></span>
<span data-ttu-id="49f2c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f2c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f2c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f2c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f2c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49f2c-127">INPUTS</span></span>

### <span data-ttu-id="49f2c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="49f2c-128">System.String</span></span>

## <span data-ttu-id="49f2c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49f2c-129">OUTPUTS</span></span>

### <span data-ttu-id="49f2c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="49f2c-130">System.Void</span></span>

## <span data-ttu-id="49f2c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49f2c-131">NOTES</span></span>

## <span data-ttu-id="49f2c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49f2c-132">RELATED LINKS</span></span>

[<span data-ttu-id="49f2c-133">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="49f2c-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


