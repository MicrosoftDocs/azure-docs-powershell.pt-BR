---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112734"
---
# <span data-ttu-id="c0339-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c0339-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c0339-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0339-102">SYNOPSIS</span></span>
<span data-ttu-id="c0339-103">Remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0339-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c0339-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0339-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0339-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0339-105">DESCRIPTION</span></span>
<span data-ttu-id="c0339-106">O cmdlet **Remove-AzOperationalInsightsSavedSearch** remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0339-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c0339-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0339-107">EXAMPLES</span></span>

### <span data-ttu-id="c0339-108">Exemplo 1: Remover uma pesquisa salva</span><span class="sxs-lookup"><span data-stu-id="c0339-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="c0339-109">Esse comando remove uma pesquisa salva do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0339-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="c0339-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0339-110">PARAMETERS</span></span>

### <span data-ttu-id="c0339-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0339-111">-DefaultProfile</span></span>
<span data-ttu-id="c0339-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c0339-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0339-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0339-113">-ResourceGroupName</span></span>
<span data-ttu-id="c0339-114">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0339-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c0339-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c0339-115">-SavedSearchId</span></span>
<span data-ttu-id="c0339-116">Especifica a ID de pesquisa salva.</span><span class="sxs-lookup"><span data-stu-id="c0339-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="c0339-117">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c0339-117">-WorkspaceName</span></span>
<span data-ttu-id="c0339-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0339-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c0339-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c0339-119">-Confirm</span></span>
<span data-ttu-id="c0339-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0339-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0339-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0339-121">-WhatIf</span></span>
<span data-ttu-id="c0339-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c0339-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0339-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0339-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0339-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0339-124">CommonParameters</span></span>
<span data-ttu-id="c0339-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0339-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0339-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0339-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0339-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="c0339-127">INPUTS</span></span>

### <span data-ttu-id="c0339-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c0339-128">System.String</span></span>

## <span data-ttu-id="c0339-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="c0339-129">OUTPUTS</span></span>

### <span data-ttu-id="c0339-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="c0339-130">System.Void</span></span>

## <span data-ttu-id="c0339-131">Notas</span><span class="sxs-lookup"><span data-stu-id="c0339-131">NOTES</span></span>

## <span data-ttu-id="c0339-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0339-132">RELATED LINKS</span></span>

[<span data-ttu-id="c0339-133">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="c0339-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


